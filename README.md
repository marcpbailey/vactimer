
# Vacuum Timer Control Blueprint for Home Assistant

This Home Assistant blueprint provides an easy way to control vacuums, pumps, or other devices on a timed schedule using a switch, timer, and input number slider.

## 🎯 Features
- Automatically starts, pauses, and stops devices.
- Tracks runtime using a **timer helper**.
- Allows resuming paused operations.
- Fully customizable with **input_number** and **timer** helpers.

## 📦 Requirements
Ensure the following helpers are created in Home Assistant:
- **Input Number**: For setting runtime duration.
- **Timer Helper**: To manage cleaning cycles.
- **Switch Entity**: For controlling the device's power state.

## 📂 Files Included
- `blueprints/automation/vacuum_timer_control.yaml`: The main blueprint.
- `configuration_fragments/input_number.yaml`: Example for runtime slider.
- `configuration_fragments/timer.yaml`: Example for the timer helper.

## 📖 Usage Instructions
1. **Import the Blueprint:** Copy the `vacuum_timer_control.yaml` file into your `config/blueprints/automation` folder.
2. **Reload Blueprints:** Go to **Developer Tools > YAML > Reload Blueprints**.
3. **Create an Automation:** Use the **Vacuum Timer Control** blueprint from the Automations UI.
4. **Configure Entities:** Select your **switch**, **timer**, and **input number** helpers.

## 📥 Installation
To clone this repository and start using the blueprint:

```bash
git clone https://github.com/yourusername/vactimer.git
```

## 🛠️ Configuration Examples
### `configuration_fragments/input_number.yaml`
```yaml
input_number:
  pool_filter_runtime:
    name: Pool Filter Runtime
    initial: 60
    min: 1
    max: 480
    step: 1
    unit_of_measurement: minutes
```

### `configuration_fragments/timer.yaml`
```yaml
timer:
  pool_filter_timer:
    name: Pool Filter Timer
    duration: "00:00:00"
```

## 📜 License
This project is licensed under the [MIT License](LICENSE).
