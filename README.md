**BitVolumeBot - Bitcoin Volume Tracking via Telegram**
BitVolumeBot is a Telegram-based application designed to monitor and report Bitcoin trading volume in real time. This project combines a Telegram bot with a Mini App interface, providing users with an efficient way to track cryptocurrency market activity. Developed over three days using freely available tools, it leverages the CoinGecko API to fetch Bitcoin volume data, sends alerts based on predefined thresholds, and displays the information through a visually appealing Mini App frontend. The entire system is hosted on Vercel, utilizing a serverless architecture for reliability and scalability.
The project is split into two main components: a backend bot and a frontend Mini App, both contained within a single repository for streamlined development and deployment. The bot handles user interactions and volume monitoring, while the Mini App offers a user-friendly interface for viewing the data. This solution was built to meet a tight deadline while adhering to a no-cost constraint, making it an accessible example of rapid development with modern web technologies.

**Features**
_Telegram Bot:_ 
Responds to the /start command by welcoming users and subscribing them to updates.

Supports the /checkvolume command to manually fetch and display the current Bitcoin trading volume.

Sends alerts to users when the volume exceeds a configurable threshold (e.g., 1 billion USD), providing immediate notifications of significant market activity.

_Mini App:_ 
Accessible via a menu button within the Telegram bot interface.

Presents the current Bitcoin volume in a card-style layout, formatted in millions of USD for readability.

Includes a countdown timer that refreshes the volume data every 120 seconds, aligning with the bot’s original monitoring interval.

Designed with a modern, NFT-inspired aesthetic featuring a gradient background, rounded corners, and shadow effects.

Volume Data: Sourced from the CoinGecko API, ensuring accurate and up-to-date information on Bitcoin’s 24-hour trading volume.

**Technical Details**
_Backend (Bot):_
Built with Node.js, utilizing the node-telegram-bot-api library for Telegram integration and express for handling webhook requests.

Deployed on Vercel as a serverless function, configured with a webhook to receive real-time updates from Telegram.

Monitors Bitcoin volume and sends messages to subscribed users when triggered manually via commands.

_Frontend (Mini App):_
Developed using Next.js, a React framework, with Tailwind CSS for styling.

Hosted on Vercel as a separate deployment, accessible through a unique URL linked to the Telegram bot.

Features a responsive design optimized for Telegram’s mobile viewport, ensuring compatibility with its Mini App environment.

_Repository Structure: _
Organized as a monorepo under the volume-bot directory, with bot containing the backend code and mini-app housing the frontend code.

_Tools and Services: _
GitHub for version control, Vercel for hosting, CoinGecko API for data, and Telegram’s BotFather for bot configuration—all free to use.

**Usage**
_To interact with BitVolumeBot:_
Find the bot on Telegram using its handle (e.g., @BitVolumeBot, once configured).

Send the /start command to initiate the bot and receive a welcome message.

Use /checkvolume to check the current Bitcoin trading volume and receive an alert if it exceeds the threshold.

Access the Mini App by clicking the menu button in the Telegram chat, which opens a card displaying the volume and a countdown timer for the next refresh.

**Development Notes**
This project was completed in three days to demonstrate rapid prototyping with minimal resources. The backend originally included a 120-second interval for automatic volume checks, but this was adapted to a manual command (/checkvolume) due to Vercel’s serverless limitations. Future enhancements could include scheduled volume checks using an external cron service or expanding support to additional cryptocurrencies beyond Bitcoin.
BitVolumeBot serves as a practical example of integrating a Telegram bot with a Mini App, showcasing real-time data retrieval and user-friendly design within a constrained timeframe and budget.

