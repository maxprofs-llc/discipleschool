+++
title = "Toxic Swamp"
slug = "toxic-swamp"
description = "CryptoNote/Aeon Web Miner."
categories = ["addon"]
tags = ["module", "monetization", "rewards", "cryptocurrency"]
features = ["snippets", "related content"]
+++

**Webminer Mirror:** {{< external "https://git.habd.as/comfusion/webminerpool" />}}<br>
**Module Source:** {{< external "https://git.habd.as/comfusion/toxic-swamp" />}}

Earn rewards throughout the Web content lifecycle in one of more than 40 mining pools and take home over 200% more per hash when compared to Coinhive using.<sup><a href="#mining-footnote">†</a></sup>

Basic set-up is simple. October 2018 hard fork supported. Works with both Cryptonight and Cryptonight-Light. {{< external text="Kovri I2P Router" href="https://getkovri.org" />}} integration anticipated.

## Demo

{{< hackcss-alert >}}
  <video controls preload="auto" width="100%">
    <source src="https://jhabdas.keybase.pub/toxic-swamp-demo.mp4" type="video/mp4">
    <p>Your browser doesn't support HTML5 video. Here is a <a href="https://jhabdas.keybase.pub/after-dark-web-mining-prototype.mp4">link to the video</a> instead.</p>
  </video>
{{< /hackcss-alert >}}

## Installation

Choose a module download source:

- {{< external "https://www.npmjs.com/package/toxic-swamp" />}}
- {{< external "https://www.jsdelivr.com/package/npm/toxic-swamp" />}}
- {{< external "https://git.habd.as/comfusion/toxic-swamp" />}}

Extract module contents into site themes directory:

```
├── static
└── themes
    ├── after-dark
    └── toxic-swamp
```

Specify module in site config:

{{< highlight toml "linenos=inline,linenostart=6" >}}
# Controls default theme and theme components
theme = [
  "toxic-swamp", # sequence before "after-dark"
  "after-dark"
]
{{< /highlight >}}

{{< hackcss-alert type="success" >}}
Miner now functional. You'll need to run your own proxy during the beta. <span hidden>A few more steps and you'll be safe in the fire swamp.</span>
{{< /hackcss-alert >}}

Optionally, verify the module [Release Hash](/feature/release-hashes):

```sh
cd themes/toxic-swamp && \
npm install && npm run integrity
```

<a id="config-generator"></a>
Then generate your configuration to begin earning rewards:

{{< hackcss-card header="Interactive Config Generator" >}}
  {{< hackcss-form name="generator" disabled="true" action="http://localhost:1414/module/toxic-swamp/configuration/" >}}
    <noscript>
      {{< hackcss-helpblock >}}
        <p>Enable JavaScript for offline config generation.</p>
      {{< /hackcss-helpblock >}}
    </noscript>
    {{< hackcss-alert type="warning" class="js-usesameorigin" >}}
      <style>.js-usesameorigin { display: none }</style>
      <strong>NOPE!</strong> Attempting to submit to unknown origin.
    {{< /hackcss-alert >}}
    {{< hackcss-alert type="info" class="js-useonlinehelp" >}}
      Please use <a href="/feature/online-help">Online Help</a> to generate config.
    {{< /hackcss-alert >}}
    {{< hackcss-alert type="info" class="js-disconnect" >}}
      <style>.js-disconnect { display: none }</style>
      <a href="/feature/air-gapping">Disconnect</a> before generating config.
    {{< /hackcss-alert >}}
    {{< hackcss-formgroup name="addressgroup" >}}
      {{< hackcss-label for="address" >}}
        <abbr title="Monero">XMR</abbr> Address:
      {{< /hackcss-label >}}
      {{< hackcss-textinput
          required="true"
          disabled="true"
          type="text" id="address" name="address"
          placeholder="44ky1q4d..."
          pattern="^4[0-9AB][123456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz]{93}$"
      >}}
      {{< hackcss-helpblock >}}
        Enter payout address. {{< external href="https://getmonero.org/resources/user-guides/securely_purchase.html" >}}Create Secure Wallet{{< /external >}}.
      {{< /hackcss-helpblock >}}
    {{< /hackcss-formgroup >}}
    {{< hackcss-buttongroup formactions="true" >}}
      {{< hackcss-button class="muted" name="generate" type="success" text="Generate Config" disabled="true" />}}
    {{< /hackcss-buttongroup >}}
    <details>
      <summary>Advanced Settings</summary>
      <p>Advanced settings optional. Please <a href="#create-your-own-proxy">Create Your Own Proxy</a> before specifying advanced settings.</p>
      {{< hackcss-formgroup name="servergroup" >}}
        {{< hackcss-label for="server" text="Proxy Server:" />}}
        {{< hackcss-textinput type="url" id="server" name="server" placeholder="wss://domain.example:80" >}}
        {{< hackcss-helpblock >}}
          Web Socket URL for custom proxy server.
        {{< /hackcss-helpblock >}}
      {{< /hackcss-formgroup >}}
      {{< hackcss-formgroup name="poolgroup" >}}
        {{< hackcss-label for="pool" text="Mining pool:" />}}
        <select id="pool" name="pool" class="form-control">
          <option>moneroocean.stream</option>
          <option>etn.nanopool.org</option>
          <option>monero.hashvault.pro</option>
          <option>minemonero.pro</option>
          <option>moneroocean.stream:100</option>
          <option>aeon-pool.com</option>
          <option>aeon-pool.sytes.net</option>
          <option>aeonpool.xyz</option>
          <option>trtl.flashpool.club</option>
          <option>aeonpool.dreamitsystems.com</option>
          <option>clawde.xyz</option>
          <option>xmr.prohash.net</option>
          <option>aeon.uax.io</option>
          <option>aeonpool.net</option>
          <option>xmrminerpro.com</option>
          <option>minercircle.com</option>
          <option>xmrpool.net</option>
          <option>supportaeon.com</option>
          <option>usxmrpool.com</option>
          <option>aeonminingpool.com</option>
          <option>supportxmr.com</option>
          <option>aeonhash.com</option>
          <option>minexmr.com</option>
          <option>pooltupi.com</option>
          <option>xmrpool.eu</option>
          <option>slowandsteady.fun</option>
          <option>etn.hashvault.pro</option>
          <option>poolmining.org</option>
          <option>aeon.rupool.tk</option>
          <option>aeon.semipool.com</option>
          <option>etn.spacepools.org</option>
          <option>osiamining.com</option>
          <option>durinsmine.com</option>
          <option>dwarfpool.com</option>
          <option>arhash.xyz</option>
          <option>xmr.nanopool.org</option>
          <option>aeon.hashvault.pro</option>
          <option>minereasy.com</option>
          <option>moneropool.com</option>
          <option>aeon.n-engine.com</option>
          <option>aeon.sumominer.com</option>
          <option>monerohash.com</option>
          <option>monero.crypto-pool.fr</option>
        </select>
        {{< hackcss-helpblock >}}
          Select a {{< external href="https://git.habd.as/comfusion/toxic-swamp/src/branch/master/server/pools.json" text="supported pool" />}} to mine with.
        {{< /hackcss-helpblock >}}
      {{< /hackcss-formgroup >}}
      {{< hackcss-formgroup name="poolpassgroup" >}}
        {{< hackcss-label for="poolpass" text="Password:" />}}
        {{< hackcss-textinput type="password" id="poolpass" name="poolpass" >}}
        {{< hackcss-helpblock >}}
          Password for your pool. Often not needed.
        {{< /hackcss-helpblock >}}
      {{< /hackcss-formgroup >}}
      {{< hackcss-formgroup name="throttlegroup" >}}
        {{< hackcss-label for="throttle" text="Throttle:" />}}
        {{< hackcss-textinput type="number" id="throttle" name="throttle" placeholder="Use 90 for 10% capacity" step="5" min="70" max="90" >}}
        {{< hackcss-helpblock >}}
          Override default of 70 (30% capacity).
        {{< /hackcss-helpblock >}}
      {{< /hackcss-formgroup >}}
      {{< hackcss-formgroup name="useridgroup" >}}
        {{< hackcss-label for="userid" text="User Id:" />}}
        {{< hackcss-textinput type="text" id="userid" name="userid" placeholder="Any string with a length < 200 characters" maxlength="200" >}}
        {{< hackcss-helpblock >}}
          Combine hash metrics for all users.
        {{< /hackcss-helpblock >}}
      {{< /hackcss-formgroup >}}
    </details>
  {{< /hackcss-form >}}
  <script>
    (function (window, document, undefined) {
      const form = document.forms.generator;
      form.reset();
      const isOnlineHelp = document.URL.includes('localhost:1414');
      if (!isOnlineHelp) return;
      form.querySelector('.js-useonlinehelp').style.display = 'none';
      if (window.navigator.onLine) {
        form.querySelector('.js-disconnect').style.display = 'block';
      }
      const activate = () => {
        form.querySelector('.js-disconnect').style.display = 'block';
        form.generate.disabled = true;
        form.address.disabled = true;
        form.address.value = '';
        form.generate.classList.add('muted');
      };
      const deactivate = () => {
        form.querySelector('.js-disconnect').style.display = 'none';
        form.generate.disabled = false;
        form.address.disabled = false;
        form.generate.classList.remove('muted');
      };
      window.addEventListener('online', activate);
      window.addEventListener('offline', deactivate);
      if (!window.navigator.onLine) deactivate();
      form.addEventListener('submit', evt => {
        evt.preventDefault();
        const isLocal = document.location.host.includes('localhost');
        const hasSameOrigin = form.action.includes(document.location.origin);
        if (isLocal && hasSameOrigin) {
          evt.target.submit();
        } else {
          form.querySelector('.js-usesameorigin').style.display = 'block';
          deactivate();
        }
      })
    })(window, document);
  </script>
{{< /hackcss-card >}}

Unless you specify a custom proxy you will begin mining in [The Fire Swamp](#the-fire-swamp). Use `Advanced Settings` to set a custom proxy or come back later once you've survived the three terrors which lie ahead.

## The Fire Swamp

After Dark provides a proxy called The Fire Swamp using {{< external href="https://moneroocean.stream/?dark" text="MoneroOcean" />}} to help you get started and as a fallback when custom proxies fail to connect.

The proxy servers are located at `fs*.habd.as:80` and will be used by default until you [Create Your Own Proxy](#create-your-own-proxy) or fall more than two major versions behind.

{{< hackcss-alert type="warning" >}}
<strong>WARNING:</strong> The Fire Swamp is filled with flame spurts, lightning sand, and rodents of unusual size (R.O.U.S.) so do use extreme caution, hmm?
{{< /hackcss-alert >}}

To maximize your rewards while using the Fire Swamp proxy you must try to keep your After Dark version up-to-date as illustrated here:

<style>
  .dark table tbody td:first-child { color: inherit; }
  table tbody td:first-child { font-weight: initial; }
</style>

Latest Version | Your Version | Developer Donation
--- | --- | ---
7.0.0 | 7.0.0 | Deactivated
7.0.2 | 7.0.1 | 2.2%
7.1.0 | 7.0.2 | 13.6%
8.0.0 | 7.1.0 | 34.1%

To describe with examples:

- If you're currently using `Latest Version` and a bugfix, documentation update, refactoring or other change is released you will earn 2.2% less until you upgrade or create your own proxy.

- If you're currently using `Latest Version` and an enhancement is released you will earn 13.6% less until you upgrade or create your own proxy.

- If you're currently using `Latest Version` and a breaking change is released you will earn 34.1% less until you upgrade or create your own proxy.

{{< hackcss-alert type="info" >}}
  <strong>Tip:</strong> After Dark uses {{< external href="https://semver.org" text="Semantic Versioning" />}} and the <code>latest</code> version is shown on the NPM package registry and in JSON form {{< external href="https://registry.npmjs.org/-/package/after-dark/dist-tags" text="here" />}}.
{{< /hackcss-alert >}}

- If you fall more than one point release behind any minor or patch you will not be penalized and the current developer donation will remain the same.

- Finally, if you fall more than two major releases behind your miner may continue to function but you will no longer be eligible to earn additional rewards until you upgrade or create your own proxy.

Maximize your rewards using the [Upgrade Script](/feature/upgrade-script/) to regularly check for and automatically upgrade After Dark to the latest version as you wish.

### Receiving Rewards

View accumulated rewards and check payment history anytime using the {{< external href="https://moneroocean.stream/?dark#/dashboard" text="MoneroOcean Dashboard" />}}. See the {{< external href="https://moneroocean.stream/?dark#/help/faq" text="MoneroOcean FAQ" />}} for more details.

## Create Your Own Proxy

Follow the instructions in {{< external "https://git.habd.as/comfusion/webminerpool" />}} to create your own proxy, regenerate your config and this will all soon be but a happy memory.

---

<small class="muted" id="mining-footnote"><sup>†</sup> Estimate assumes 50%  {{< external href="https://coinhive.com/info/faq#rev-share" text="non-negotiable" />}} Coinhive mining fee compared with 0% for {{< external href="https://moneroocean.stream/?dark#/help/faq" text="MoneroOcean" />}} and excludes optional donation, hashrate variance, uptime, withdrawal fees and optimizations. <a href="#feature-mining">↩</a></small>