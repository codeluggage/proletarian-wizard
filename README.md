# proletarian-wizard README

Proletarian Wizard helps you organize your notes within a GTD-like organized set of folders. It provides two main sets of features:
- File management, organizing files into an opinionated set of folders and files
- Todo management, collecting todos from project notes. This is admitting that the distinction between notes and todos is not as clear as it seems, and that these todos still need robust organization.

## Extension Settings

App requires the folder structure to be the following:

- 10 - Inbox - All files you create in a hurry and didn't sort yet
- 20 - Current Projects - Groups of files related to a given project
- 21 - Recurrence - Notes from recurring meetings
- 30 - Reference - Reference files
- 40 - Archived Projects - Projects that are no longer active

**Config file**: Add a file `.pw/config.yml` with the following structure to configure the folders:

```yaml
config:
  folders:
    inbox: INBOX_FOLDER_NAME # relative to the root folder
    projects: CURRENT_PROJECTS_FOLDER_NAME
    recurrences: RECURRENCES_FOLDER_NAME
    reference: REFERENCE_FOLDER_NAME
    archive: ARCHIVED_PROJECTS_FOLDER_NAME
```

**Templates**: To use templates, create a folder `.pw/templates` in your root folder, and put templates there. They can embed variables using the format `${Variable name}` which will be prompted upon creation of a note from the template. To use templates, use the command `Proletarian Wizard: Create Note from Template`

## Todo

Proletarian Wizard also includes a todo management system. These are displayed in an explorer window called "todo hierarchy". Any markdown file with a line following this format:

```markdown
[ ] This is a todo
```

Boxes can be toggled using `alt+enter`

will be considered as a todo. In the box, the following values are use:
- `x` when completed. PW provides a shortcut: `Alt+x`
- `d` when delegated: `alt+d`
- `-` when in progress: `alt+-`
- `!` when attention is required `alt+shift+!`
- `space` when todo `alt+t`
- remove the space, when cancelled: `alt+c`

PW also supports inline attributes, using the following format: `@attributename(attribute value)`. These are used for display in the explorer window.

There is one special attribute called `selected` which allows you to pick some tasks you want to keep in front (say, for example, those you want to process today, or this week).

## Features

- [x] Save files in the correct place in few keystrokes
- [ ] Support several layers of folders
- [x] Open files with a few keystrokes
- [x] Create files from templates
- [x] Create projects
- [x] Archive projects
- [ ] Create files directly in projects
- [x] Define custom paths for directories
- [ ] List files from tags
- [x] Create recurrences
- [x] Create reference folders
- [x] Prompt variables in templates
- [x] Use "this folder"
- [x] Include recurrence name in new note by default
- [x] Add date in line
- [x] Support todo status
- [x] List all todos across workspace
- [x] Grouping todos by project
- [x] Save display preferences
- [x] Support line attributes (assignee, priority, due date, selected)
- [ ] Group by attributes
- [x] Display "@selected" on top
- [ ] Optimize reload of todos
- [ ] When clicking on todo, open file at the right line
- [ ] Support `@project` attribute for todos in the wrong folder
- [ ] Show projects on top of list of todos
- [ ] Support tags for todos, group by tags 
- [ ] Support project briefs, use as project name
- [ ] Autocomplete attribute names and attribute values

## Known Issues

_Nothing yet_

## Release Notes

### 0.9.0

- Group view by state or project
- Display task status as icon
- Support in-line attributes (use @attributeName(attributeValue))
- Show selected todos on top (add an @selected attribute to the todo)

### 0.8.0

- Add view listing todo items by state

### 0.7.0

- Add keyboard shortcuts for todo management

### 0.5.0

- Add date to current line
- Manage todo status (todo, in progress, delegated, attention required, cancelled, completed)

### 0.3.0

- For recurrence, default file name includes the name of the recurrence.

### 0.2.0

- Support `<this folder>` as a choice for save, archive, ... Also support archiving files.

### 0.1.0

- Create recurrence folder
- Create reference folder
- Define custom path for folders in config file
- Prompt for variables when loading a template.

### 0.0.1

- Save files in right folder.