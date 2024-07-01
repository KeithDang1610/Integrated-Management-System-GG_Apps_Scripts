# Integrated-Management-System-GG_Apps_Scripts
## Context:
Traditionally, students who want to borrow equipment (such as tools or machines) for extra practice must meet with a manager or teacher to make a request. This can be inconvenient due to the potential absence of the manager, leading to wasted time for students who have to come back later. To address these issues, an online system has been developed to automate and streamline the process.
### Challenges:
- Non-Budget: The system was developed without a budget, requiring the use of free platforms and tools.
- System Flow Complexity: Implementing a smooth system flow using free platforms like Google Sheets presented significant difficulties.
- Lack of Knowledge: There was no prior knowledge of Google Apps Script, which was necessary to automate various parts of the system.
- Data Characteristics: The special characteristics of the data source and data entry process posed challenges in ingesting data into the system without altering the input format significantly.

<img src="https://github.com/KeithDang1610/Integrated-Management-System-GG_Apps_Scripts/assets/167521177/5773353c-ed64-4879-af39-d80842804f05.pnp" width=70% height=70%>

- The colors represent different experiment modules, such as Turning, Milling, and Planning.
- The text value inside each cell indicates the teacher's name.
- There are two sessions each day: the morning session and the afternoon session, with each session consisting of five class periods.

- Integration of Multiple Google Features: Combining multiple Google services (Google Drive, Google Sheets, Google Forms, Google Calendar, and Google Apps Script) into a cohesive system required considerable effort

## Acknowledgment:
- **Mr. Kurt Kaiser**: Thank you to Mr. Kurt Kaiser, who published free open-source materials on the Internet. These resources were instrumental in helping me understand and follow the necessary steps. His source codes for management function sheets were particularly useful as a foundation. I was able to integrate my custom codes and develop additional sheets (import sheet, checking sheet, export sheet), greatly enhancing my problem-solving, analytical thinking, and coding skills, especially in - Google Apps Script, which is very similar to JavaScript.
- **Google Institute**: Thank you to Google for providing a wide array of free services that have been invaluable in optimizing, automating, and leveraging our work.

## System Overview:
The system consists of two main components: one for users (students) and one for managers (teachers or lab instructors). The managers are responsible for ensuring that students have access to adequate facilities for practice.

## Progress Flow Explanation:

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/9ba163b4-b2db-4d82-9fc4-96aff3a459bf.pnp" width=70% height=70%>

### Input (Managers/Teachers):

Managers import class schedules into a Google Calendar using an import function sheet. This includes details such as class sessions, teacher names, dates, modules (each module associated with specific machine types like lathes or milling machines), and the number of available machines.

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/b27367fd-87d2-4a1a-9fe9-d57d2880d0f1.pnp" width=70% height=70%>

### Input (Students):

Students who need extra practice can check the schedule using a checking function sheet to find available machines.

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/7212ee40-7be9-4863-8bf3-ca73543ee42a.pnp" width=70% height=70%>

Students register by filling out a Google Form, which ingests their information into a management function sheet. They will receive a conflict notification email if they skip the checking step and try to register for an occupied slot.

- The template of a received email

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/b86cefaf-0826-4b82-a1d3-64c6d8ebd265.png" width=50% height=50%>


### Process:

Managers receive email notifications for new user registrations. They can review user information later if they are busy.
After considering the requests, managers approve or deny them. Approved requests trigger an automatic email to the student confirming the reservation, while denied requests prompt a fail email, allowing the student to send another request.
  
### Output:

Periodically, managers or accessible teachers can extract detailed information from the Google Calendar using an export function sheet. This detailed data is used for evaluation and arranging maintenance schedules.
<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/1e301911-b800-4e67-af57-b1706e09808d.pnp" width=70% height=70%>

## The results:
### Checking function sheet:

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/7212ee40-7be9-4863-8bf3-ca73543ee42a.pnp" width=70% height=70%>
- Students can inspect the empty schedules online using this sheet

### Import Function sheet:

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/b27367fd-87d2-4a1a-9fe9-d57d2880d0f1.pnp" width=70% height=70%>

- This sheet is user-friendly and can be easily accessed and utilized by anyone, regardless of their technical expertise. Even the manager can use it with minimal instruction.
- It reduces operational time by 80% compared to manual handling. For instance, it used to take almost 4 hours to input data into a spreadsheet manually. Now, with simple steps and an easily accessible interface, the same task can be completed in just 15-20 minutes, ensuring careful data entry.

### Management Function sheet:

<img src="https://github.com/KeithDang1610/Integrated-Management-System-GG_Apps_Scripts/assets/167521177/05c27b88-6573-495b-ba6e-b3300544f048.pnp" width=70% height=70%>

Data from the booking form is stored in this sheet and undergoes assessment by the manager. Following the assessment, an email is automatically sent to the user indicating approval or rejection. In cases of conflicts, a notification email is instantly sent when this sheet is run.

### Export Function sheet:

<img src="https://github.com/KeithDang1610/Management-Integrated-System-GG_Apps_Scripts/assets/167521177/1e301911-b800-4e67-af57-b1706e09808d.pnp" width=70% height=70%>

This sheet will return the result (all information about schedules and classes in the Lab workshop), extracted from the Google Calendar.

### Another Export Function sheet:

<img src="https://github.com/KeithDang1610/Integrated-Management-System-GG_Apps_Scripts/assets/167521177/d33c8b33-0103-4463-87bc-ce4855eedb2c.pnp" width=70% height=70%>

This sheet is quite different from the previous sheet, The formats and types of data will be changed automatically by extracting from the Calendar and processing with Apps Scripts.

## Skill gained:

- Problem-Solving
- Analytical Thinking
- data analysis
- Coding Skills
- System Mindset

## Conclusion
This project presented many challenges, requiring relentless effort and research. However, with patience and curiosity, I was able to successfully complete it. The system offers several significant improvements:

1. **Time Efficiency**: Data entry time has been reduced by 80%, from almost 4 hours to just 15-20 minutes.
2. **Accuracy**: Ensures accurate data entry, minimizing human errors.
3. **Convenience for Students**: Students can now easily register online, improving the registration process.
4. **Remote Management**: Managers can make decisions and manage tasks from a distance, eliminating the need for constant physical presence.
5. **Automated Notifications**: Automatic emails for approvals, rejections, and conflict notifications streamline communication.
6. **Cost-Effective**: The system is free, making it an accessible solution for everyone involved.

Overall, this system not only assists in data entry but also significantly enhances operational efficiency and convenience, especially since it is free.
