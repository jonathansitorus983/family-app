FamilyFlow

A family schedule management app built as a single, self-contained HTML file. No installation, no login, no dependencies to install — just open familyflow.html in any modern browser and you're ready to go.


Getting started


Download familyflow.html
Double-click to open it in your browser (Chrome, Firefox, Safari, or Edge all work)
That's it


No internet connection is required after the first load. The app loads two small external resources on startup — the Inter font and Tabler icons — so the first open looks best with a connection. After that it works fully offline.


What's inside

Three views

Calendar — a week-at-a-glance grid showing every family member's events color-coded by person. Navigate forward and backward through weeks using the arrow buttons, or jump back to the current week with the Today button.

Upcoming — a card-based feed showing today's events followed by the rest of the week. Each card shows who's involved, the time, and the category. Click any card to see full details in the side panel.

Overview — a weekly summary with event counts, a visual breakdown of events by person, smart conflict alerts (like overlapping pickup times), and a busiest-days bar chart.

Family members

The app comes pre-configured for the Henderson family with four members:

MemberColorRoleSarahCoralParentMarkSageParentEmmaVioletAge 12LiamSkyAge 8

Each person has a consistent color throughout the app — on the calendar, in chips, in cards, and in the detail panel — so anyone can scan the schedule at a glance.


Features

Adding events

Click Add event in the top bar or the left nav (or press N on your keyboard) to open the add-event form. You can set:


Title and category (School, Sports, Work, Medical, Social, Family, Other)
Date, start time, and end time
Location
Which family members are involved (select one or more)
A color label
Notes (pickup instructions, what to bring, etc.)
Whether the event repeats weekly, biweekly, or monthly


Viewing event details

Click any event on the calendar or any card in the Upcoming view to slide open the detail panel on the right. It shows the full title, time, who's involved, and any notes. From there you can edit or remove the event.

Filtering by person

On the Calendar view, use the filter chips below the week navigation to show only one person's events. You can also click a family member's name in the left sidebar to jump straight to their filtered calendar.

Conflict alerts

The Overview tab automatically flags days where two events might clash — for example, if a child's activity overlaps with a pickup time. These appear as amber warning cards.


Keyboard shortcuts

KeyActionNOpen the add-event formEscClose any open modal or detail panel


Customising the family

To change names, colors, or add more family members, open familyflow.html in a text editor and search for Henderson. The family members are defined in a few places — the sidebar, the filter chips, and the member-check rows in the modal. Each is straightforward HTML you can edit directly.

Color variables are defined at the top of the <style> block under :root. The five named colors are:

--coral   #E8644A
--sage    #5A8A6E
--gold    #C4843A
--violet  #6B5EA8
--sky     #3A7FC4


Browser support

Works in any modern browser. Tested in Chrome 120+, Firefox 120+, Safari 17+, and Edge 120+. Responsive down to mobile screens — on small viewports the sidebar collapses into a compact bottom navigation bar.


File structure

Everything lives in a single file:

familyflow.html
├── <style>        CSS with custom properties, layout, and responsive rules
├── <main>         App shell — sidebar, topbar, and three tab panels
├── Modals         Add-event dialog and event detail slide-in panel
└── <script>       Tab switching, filtering, week navigation, modal logic

No build tools, no frameworks, no package.json. Edit the file directly to make it your own.


Design notes

FamilyFlow was designed with a clean, editorial aesthetic inspired by Shabnam Kashani's portfolio — generous whitespace, confident typography, and minimal chrome that stays out of the way. The color system uses five distinct hues (never more than one per person) so the schedule communicates ownership before you read a word.

