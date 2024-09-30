# Bubble-Dashboard
This dashboard is designed for **Home Assistant** using [**Bubble Cards**](https://github.com/Clooos/Bubble-Card) to provide an intuitive and visually appealing interface. It is fully **adaptive** to different screen resolutions, ensuring a consistent user experience across devices. The setup is customizable, making it easy to tailor the layout and features to your smart home needs.
<br>

## Table of contents

**[`Installation`](#installation)**  **[`Configuration`](#configuration)**
<br>
## Installation

**Home Assistant lowest supported version:** 2023.9.0

<details>

<summary>Prerequisites</summary>

<br>

1. [Bubble Cards](https://github.com/Clooos/Bubble-Card)
2. [Bubble Theme](https://github.com/UberDudepl/Bubble)
3. [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
4. [State Switch](https://github.com/thomasloven/lovelace-state-switch)
5. [Layout Card](https://github.com/thomasloven/lovelace-layout-card)

</details>

In order to fully replicate this dashboard in your Home Assistant, the following items need to be installed:

<details>

<summary>Optional</summary>

<br>

1. [Waste Collection Schedule](https://github.com/mampfes/hacs_waste_collection_schedule)
2. [SmartThinQ LGE Sensors](https://github.com/ollo69/ha-smartthinq-sensors)
3. [Frigate](https://github.com/blakeblackshear/frigate-hass-integration) & [Frigate Card](https://github.com/dermotduffy/frigate-hass-card)
4. [RGB Light Card](https://github.com/bokub/rgb-light-card)
5. [SmartThing Custom](https://github.com/veista/smartthings)
6. [Light Entity Card](https://github.com/ljmerza/light-entity-card)
7. [Decluttering Card](https://github.com/custom-cards/decluttering-card)
8. [Stack in Card](https://github.com/custom-cards/stack-in-card)

</details>

The installation process is straightforward. Follow these steps to set up the dashboard:

1. **Create a `views` folder**:  
   - If you're using the **Studio Code Server Add-on** for Home Assistant (recommended), navigate to your Home Assistant configuration folder.
   - Create a new folder called `views` to store your dashboard files.

2. **Modify `configuration.yaml`**:  
   Add the following code to your `configuration.yaml` file to set up a custom dashboard mode:
   
   ```yaml
   lovelace:
     mode: storage
     dashboards:
       lovelace-yaml:
         mode: yaml
         title: uberDash
         icon: mdi:account-supervisor-circle
         show_in_sidebar: true
         filename: uberdash.yaml
   ```

   This will create a custom Lovelace dashboard called **uberDash** that will appear in the sidebar with the specified icon.

3. **Copy the dashboard files**:  
   Download or clone the repository and place the dashboard YAML file (`uberdash.yaml`) in main folder and any other necessary files into the `views` folder.

4. **Configure Lovelace UI**:  
   - Open Home Assistant and navigate to **Configuration > Lovelace Dashboards**.
   - Ensure that the `uberdash.yaml` file is loaded as a new Lovelace dashboard.

5. **Adjust resources**:  
   Ensure that the Bubble Cards and other custom cards are properly referenced in your Lovelace resources (`Configuration > Lovelace Resources`).

6. **Restart Home Assistant** for the changes to take effect.

## Configuration

