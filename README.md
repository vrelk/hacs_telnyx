<img src="screenshots/telnyx-logo.png" alt="Telnyx Logo" title="Telnyx Logo" width="500"/>

# Unofficial Home Assistant integration

This integration adds the possibility of sending SMS via [Telnyx](https://www.telnyx.com).

## Installation

### Manually

Clone the repository to a folder called "custom_components" in your Home
Assistant root directory, e.g. `git clone https://github.com/vrelk/hacs ~/.homeassistant/custom_components/telnyx`

### Via [HACS](https://hacs.xyz/)
- Navigate to HACS -> Integrations -> Custom repositories -> Add
- Set *Repository* to **https://github.com/vrelk/hacs**
- Set *Type* to **Integration**
- Confirm form submission and the repository should be appended to the list

## Configuration

Add to `configuration.yaml` - usually in `~/.homeassistant/`:

```yaml
notify:
  - platform: telnyx
    sender: +13115552368 # must be a telnyx number in the form +13115552368
    name: telnyx_sms
    api_key: INSERT_YOUR_TELNYX_API_KEY_HERE
    recipient: +13115552367 # or specify multiple numbers e.g. [+13115552367, +13115552368]
```

Check out the [example](./screenshots/automation_action_call_service.png) on how to
configure a service call on automation.

## Support

[![MIT](https://img.shields.io/badge/License-MIT-teal.svg)](LICENSE)
