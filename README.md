# MVBASIC-plus-plus

## Notepad-plus-plus-D3
This is a fork of the [Notepad-plus-plus-D3 project by Remington Richards](https://github.com/Artifex-Latronis/Notepad-plus-plus-D3), significantly enhanced and extended from D3 for all MV platforms. Sincere thanks are extended to Remington for his inspiration and initial effort on this. I hope he will be interested in further collaboration on this.

The goal of this project is to provide syntax highlighting and other benefits to MVBASIC developers through the [Notepad++](https://notepad-plus-plus.org/) application.

The concept of a User Defined Language (UDL) and a style in Notepad++ are essentially the same. Each XML file in this package represents a different style which can be applied to a single language (MVBASIC dialect). Rather than customizing one of the above files, it is recommended that new styles be saved as a new UDL, so that the definitions here remain consistent base-line examples.

The MVD3_Python_D UDL is styled with color schemes that somewhat mirror python, as our community will be seeing that in the future. Note the pattern of the filename:

- "MV" ensures all MVBASIC UDL files are grouped together in a folder.
- "D3" identifies the variant. QM and UV are being tested.
- "Python" is the name of this specific styling. Contributions are welcoe here with any unique name.
- "D" indicates this is best used with a Dark theme. "L" indicates it's best used with a Light theme.

## Installation

Copy the D3Language.xml file from this project to:
"C:\Users\username\AppData\Roaming\Notepad++"
In Notepad++, go to menu>Language>Define your language...
In the User Defined Language dialog, click Import.
Navigate to the above folder and open one of the MV XML files.
A small dialog should confirm "Import Successful".
X to close the dialog.
Exit and restart Notepad++.

## Usage

Copy/Paste D3 BASIC code into the editor.
Go to menu>Language> ... Names  should be at the bottom.
Select one of the styles and the current window will re-style according to the current definition.

By default the UDLs are set to activate when specific file extensions are opened. These are as follows, and can be changed as desired.

- For D3: d3, d3basic
- For QM: qm, qmb, qmbasic
- For Universe: uv, uvb, uvbasic

## Personalizing Installed UDLs

Open BASIC code in the active edit window and select a UDL.
Go to menu>Language>Define your language...
In the User Defined Language dialog, open the "User language" dropdown, select the current UDL.

As seen in the User Defined Language dialog, there is a link to [Documentation](https://ivan-radic.github.io/udl-documentation/) with details about how UDLs work. There are many [tutorials](https://www.google.com/search?q=notepad%2B%2B+user+defined+language+tutorial) on the topic of UDLs. The information here includes detail not in that documentation, and which applies specifically to the MVBASIC UDLs.

### General

Changes in the User Defined Language dialog are saved immediately. There is no Save button.

The Styler buttons open a Styler Dialog. Settings in the styler dropdowns may not change immediately unless you use the dropdown selector to trigger a change event - just entering text and tabbing away may not fire that change event. The editor should immediately reflect changes made in these settings. Click OK to save the Styler Dialog.

It should be noted that the styling abilities in Notepad++ are [limited](http://docs.notepad-plus-plus.org/index.php/Limitations_Of_User_Defined_Languages), and the UDL editor is also limited. Some nuances of MVBASIC syntax may not fit with these limitations at this moment. For improvements in this area, file an Issue report in the Github repo for this package. If the software precludes the desired styling, check with the Notepad++ user/developer community. As a last resort, file an enhancement request for Notepad++, and when new features are available someone may update the UDLs here to benefit.

### Folder & Default tab

The Default style is applied to whatever is not identified as a keyword, which should in all cases be a variable. If a keyword is found that is not styled, please create an Issue report in the Github repo.

To change the styling for variable names, click the Styler button and change coloring or other details as desired.

Nothing else on this tab is related to MVBASIC UDLs.

### Keyword Lists tab

Keywords are organized into groups. To change the styling for a keyword, find it in a group and click the related Styler button. 

The grouping of keywords was done rather subjectively. Grouping can be dependent on how how keywords are used. For example, they can be grouped based on how they relate to one another, like WRITE and ON, IF and THEN, or LOOP WHILE UNTIL DO REPEAT. But READ, WRITE, and DELETE are file operations, so maybe they should get their own grouping. And yet, DELETE and LOCATE can be statements or functions, but there is no READ or WRITE function. So there is no absolute correct grouping, it's a matter of preference. If you disagree with how they are organized, please create an Issue report in the Github repo for peer consideration.

Since this is all very subject to personal preference, signficant changes can be exported into a new UDL and contributed to this package. 

### Comment & Number tab

The only field that applies to MVBASIC is the Line comment position which has been set to Allow Anywhere.

### Operators & Delimiters

Please refer to the [Documentation](https://ivan-radic.github.io/udl-documentation/) for details about how operators are detected and processed.

Delimiters 1-3 define how quoted text is styled when delimited by double-quotes, single-quotes, and back-slashes. Other delimiters describe styling for parentheses, including CRT @() notation.

## Updating Notepad++ from this repo

During the Import operation, files in this package are merged into a single XML file. After this they are not used. To update Notepad with new style definitions, use the UDL dialog to Remove existing definitions, then Import the replacements. A new definition cannot be imported when an existing definition has the same name.

## To Do:

- Improve the initial default D3 styling for light backgrounds.
- Look at the additional data provided by Richard.
- Verify all keywords and operators.
- Look for more detail on NPP styling which might improve syntactic parsing for MVBASIC.
- Move this ReadMe detail to wiki pages.
- Create a single wiki page to describe all available UDLs with a screenshot.
- Write notes on direct interfaces with MV to eliminate copying code out, modifying, then copying back into MV for compilation and testing.
- Look into options for code folding and other features available in other languages.

## Reporting Issues

There are at least four characteristics of these UDLs for MVBASIC:

- All MVBASIC UDLs must agree on a common understanding of MVBASIC syntax. If there is a fundamental issue in this area with one UDL it may apply to all of them.
- That said, when reporting an Issue with styling, please be specific as to whether the issue is with MVBASIC, or the platform-specific dialect.
- The grouping of keywords is subject to preference and baseline UDLs will not be changed in this package unless it's really "wrong".
- Similarly styling is entirely subjective nd should only be changed in this package if, for example, code is invisible over the background recommended for it.

With all this in mind, please be discerning about reporting "Issues". The addition of a new UDL that addresses specific tastes might be of more value to this project than a change to the core UDLs which some developers might see as a downgrade.

## License

There was no license with the original code. Unless there is disagreement from the originator, this is licensed under the [Free Public License 1.0.0](https://opensource.org/licenses/FPL-1.0.0) (The simplest official license possible.)