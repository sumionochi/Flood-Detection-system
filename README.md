# SATML & LORA Damage Response

## Inspiration
The inspiration behind the **SATML & LORA Damage Response** project stemmed from the recurring challenges faced by flood-prone areas like Myanmar. Natural disasters, especially floods, have devastating impacts, and often, communication networks are the first to fail. This leaves victims isolated from rescue and support systems. Recognizing this critical gap, we set out to design a resilient, tech-driven solution that could operate both online and offline. We envisioned a system that leverages advanced machine learning and communication technologies to save lives, optimize resource deployment, and streamline flood response management, ultimately making disaster response more effective and accessible.

## What it does
Our solution integrates three key components: satellite-based machine learning, LoRa communication, and drone deployment. Here's how each element contributes:

- **Satellite-Based Machine Learning**: We utilize a U-Net model with masking that processes satellite imagery in real-time. This enables rapid detection and prioritization of flood-affected areas, helping identify critical zones needing immediate intervention.
  
- **LoRa Communication for Offline Victim Communication**: Using a low-range wide-area network (LoRa), flood victims can communicate with authorities even when regular cellular networks are down. LoRa enables two-way communication, allowing victims to send emergency alerts and receive survival information.
  
- **Automated Drone Deployment**: To address resource delivery challenges, we deploy drones that are directed via a centralized dashboard. These drones can transport supplies and resources to the most affected areas, ensuring timely and efficient aid distribution.

Together, these components create a robust, crowd-sourced disaster management system capable of functioning in challenging environments where traditional methods might fall short.

## How we built it
We approached the project in several phases:

1. **Machine Learning Model Development**: Using U-Net architecture, we trained a model on satellite imagery data to recognize flood-impacted regions. This model was fine-tuned for real-time processing, enabling quick identification and prioritization of areas needing assistance.
  
2. **LoRa Communication Network**: We designed and implemented a LoRa-based communication module for offline victim communication. This system includes both a victim module and an organization module, which are built on Arduino platforms (Arduino Nano ESP32 for the organization module and Arduino Uno for the victim module). This setup enables victims to reach out to rescue teams even without network coverage.

3. **PLUTO AI Integration**: We created PLUTO AI, a large language model with 8 billion parameters fine-tuned for disaster response. PLUTO processes incoming data, assesses severity, and supports prioritization in real-time. It is embedded in the victim mobile application for localized emergency guidance.

4. **Drone Deployment System**: The final stage involved building an automated drone deployment system integrated into a dashboard. This system is designed for real-time resource deployment to the prioritized zones, leveraging LoRa communication for continuous updates.

5. **Centralized Data Management with Firebase**: To ensure that all data is accessible and secure, we implemented Firebase for centralized data storage. This supports rapid decision-making by providing a single source of truth for authorities and response teams.

## Challenges we ran into
Building SATML & LORA Damage Response was not without its challenges:

- **Offline Functionality**: Ensuring reliable offline communication via LoRa in disaster-prone areas required meticulous testing and adjustments to the network range and security protocols.
  
- **Data Processing in Real Time**: Processing satellite data quickly enough to make timely rescue decisions was challenging, requiring us to optimize our U-Net model and streamline data integration.
  
- **Integrating Multiple Systems**: Coordinating between LoRa modules, machine learning, and drone systems in real-time posed significant integration challenges, requiring rigorous testing and iteration to ensure seamless communication.
  
- **Power Constraints**: As the system is designed for disaster scenarios, power availability is limited. Optimizing power consumption in LoRa modules and victim devices was crucial to maintain extended offline operation.

## Accomplishments that we're proud of
- **Resilient Offline Communication**: Successfully establishing a robust offline communication network using LoRa was a significant achievement. This system ensures that even isolated individuals can connect with rescue teams.
  
- **Real-Time Disaster Mapping**: Our machine learning model can process satellite imagery in real-time, identifying critical areas faster than conventional methods.
  
- **Custom Drone Deployment System**: We developed a fully automated drone response mechanism, enabling precise, timely resource distribution.
  
- **PLUTO AI**: Creating PLUTO AI, a custom large language model tailored for disaster scenarios, was an innovative step, allowing real-time prioritization and management of data for effective decision-making.

## What we learned
This project offered valuable insights into the practical challenges of building resilient disaster response solutions:

- **Complexity of Offline Systems**: We learned a great deal about the intricacies of offline communication networks and the limitations posed by power and range constraints.
  
- **Interdisciplinary Integration**: Working with diverse technologies like machine learning, LoRa, and drone systems highlighted the importance of interdisciplinary skills and systems integration.
  
- **Importance of Real-Time Data Processing**: Effective disaster response relies on fast, accurate data. We saw firsthand the value of optimizing machine learning models for speed and accuracy.
  
- **Scalability Concerns**: Designing a scalable system that can adapt to various environments and disaster types taught us to think beyond immediate solutions and consider long-term flexibility.

## What's next for SATML & LORA Damage Response
The future roadmap for SATML & LORA Damage Response includes:

- **Expanding Data Sources**: Integrating additional data sources, such as river sensors and weather data, to improve prediction accuracy.
  
- **System Scalability**: Scaling the system to handle larger disasters and potentially expanding beyond Myanmar to other disaster-prone regions.
  
- **Enhanced Drone Capabilities**: Improving drone response by adding more sophisticated navigation capabilities and payload options.
  
- **User Interface Improvements**: Refining the user interface on both the victim and responder ends to improve usability, especially in high-stress environments.
  
- **Cost Reduction**: Reducing the cost of deployment through hardware optimization, making the system accessible to a broader audience and easier to implement in resource-limited areas.
