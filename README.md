## Bot for Conference Room Reservation

Since people in my company started using Skype for room reservation, 
this bot will be useful for reserving conference rooms in an office.

### Design Details

1. Use [FullCalendar](https://fullcalendar.io/download/) to design the **single page** web app  
   showing the current room reservations for the selected month/year.  
   [Another article on SSE](http://www.developerdrive.com/2012/03/pushing-updates-to-the-web-page-with-html5-server-sent-events/)
1. Use [HTML5 Server send events](https://dzone.com/articles/html5-server-sent-events) to update any open calendar page from connected clients.
1. Use [electron-config module](https://github.com/sindresorhus/electron-config) for persisting calendar data.  
   Any changes to the calendar have to be handled separately as a new node event type.
1. Start with simple regex based parsing of chat text to find out the **intent of the message**.  
   Later we can add [Microsoft's Language Understanding Intelligence Srevice (LUIS)](https://www.luis.ai/home/index)

## Other References

1. [How a bot framework works?](https://docs.microsoft.com/en-us/bot-framework/overview-how-bot-framework-works)
1. [Create a bot with Botbuilder SDK for NodeJS](https://docs.microsoft.com/en-us/bot-framework/nodejs/bot-builder-nodejs-quickstart)
1. [Register a bot with bot framework](https://docs.microsoft.com/en-us/bot-framework/portal-register-bot)
1. [Deploy a bot to the cloud](https://docs.microsoft.com/en-us/bot-framework/deploy-bot-overview)