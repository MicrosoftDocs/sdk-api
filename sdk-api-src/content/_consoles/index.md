---
UID: TP:consoles
ms.assetid: e2ee7d34-cf62-39b7-9826-a00785a4348a
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Consoles



Overview of the Consoles technology.

To develop Consoles, you need these headers:

 * [wincon.h](..\wincon\index.md)
 * [winuser.h](..\winuser\index.md)

For the programming guide, see [Consoles](https://review.docs.microsoft.com/en-us/win32-test/consoles).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AddConsoleAliasA function](..\wincon\nf-wincon-addconsolealiasa.md) | Defines a console alias for the specified executable. |
| [AddConsoleAliasW function](..\wincon\nf-wincon-addconsolealiasw.md) | Defines a console alias for the specified executable. |
| [AttachConsole function](..\wincon\nf-wincon-attachconsole.md) | Attaches the calling process to the console of the specified process. |
| [CreateConsoleScreenBuffer function](..\wincon\nf-wincon-createconsolescreenbuffer.md) | Creates a console screen buffer. |
| [FillConsoleOutputAttribute function](..\wincon\nf-wincon-fillconsoleoutputattribute.md) | Sets the character attributes for a specified number of character cells, beginning at the specified coordinates in a screen buffer. |
| [FillConsoleOutputCharacterA function](..\wincon\nf-wincon-fillconsoleoutputcharactera.md) | Writes a character to the console screen buffer a specified number of times, beginning at the specified coordinates. |
| [FillConsoleOutputCharacterW function](..\wincon\nf-wincon-fillconsoleoutputcharacterw.md) | Writes a character to the console screen buffer a specified number of times, beginning at the specified coordinates. |
| [FlushConsoleInputBuffer function](..\wincon\nf-wincon-flushconsoleinputbuffer.md) | Flushes the console input buffer. All input records currently in the input buffer are discarded. |
| [FreeConsole function](..\wincon\nf-wincon-freeconsole.md) | Detaches the calling process from its console. |
| [GenerateConsoleCtrlEvent function](..\wincon\nf-wincon-generateconsolectrlevent.md) | Sends a specified signal to a console process group that shares the console associated with the calling process. |
| [GetConsoleAliasA function](..\wincon\nf-wincon-getconsolealiasa.md) | Retrieves the text for the specified console alias and executable. |
| [GetConsoleAliasExesA function](..\wincon\nf-wincon-getconsolealiasexesa.md) | Retrieves the names of all executable files with console aliases defined. |
| [GetConsoleAliasExesLengthA function](..\wincon\nf-wincon-getconsolealiasexeslengtha.md) | Retrieves the required size for the buffer used by the GetConsoleAliasExes function. |
| [GetConsoleAliasExesLengthW function](..\wincon\nf-wincon-getconsolealiasexeslengthw.md) | Retrieves the required size for the buffer used by the GetConsoleAliasExes function. |
| [GetConsoleAliasExesW function](..\wincon\nf-wincon-getconsolealiasexesw.md) | Retrieves the names of all executable files with console aliases defined. |
| [GetConsoleAliasW function](..\wincon\nf-wincon-getconsolealiasw.md) | Retrieves the text for the specified console alias and executable. |
| [GetConsoleAliasesA function](..\wincon\nf-wincon-getconsolealiasesa.md) | Retrieves all defined console aliases for the specified executable. |
| [GetConsoleAliasesLengthA function](..\wincon\nf-wincon-getconsolealiaseslengtha.md) | Retrieves the required size for the buffer used by the GetConsoleAliases function. |
| [GetConsoleAliasesLengthW function](..\wincon\nf-wincon-getconsolealiaseslengthw.md) | Retrieves the required size for the buffer used by the GetConsoleAliases function. |
| [GetConsoleAliasesW function](..\wincon\nf-wincon-getconsolealiasesw.md) | Retrieves all defined console aliases for the specified executable. |
| [GetConsoleCursorInfo function](..\wincon\nf-wincon-getconsolecursorinfo.md) | Retrieves information about the size and visibility of the cursor for the specified console screen buffer. |
| [GetConsoleDisplayMode function](..\wincon\nf-wincon-getconsoledisplaymode.md) | Retrieves the display mode of the current console. |
| [GetConsoleFontSize function](..\wincon\nf-wincon-getconsolefontsize.md) | Retrieves the size of the font used by the specified console screen buffer. |
| [GetConsoleHistoryInfo function](..\wincon\nf-wincon-getconsolehistoryinfo.md) | Retrieves the history settings for the calling process's console. |
| [GetConsoleOriginalTitleA function](..\wincon\nf-wincon-getconsoleoriginaltitlea.md) | Retrieves the original title for the current console window. |
| [GetConsoleOriginalTitleW function](..\wincon\nf-wincon-getconsoleoriginaltitlew.md) | Retrieves the original title for the current console window. |
| [GetConsoleProcessList function](..\wincon\nf-wincon-getconsoleprocesslist.md) | Retrieves a list of the processes attached to the current console. |
| [GetConsoleScreenBufferInfo function](..\wincon\nf-wincon-getconsolescreenbufferinfo.md) | Retrieves information about the specified console screen buffer. |
| [GetConsoleScreenBufferInfoEx function](..\wincon\nf-wincon-getconsolescreenbufferinfoex.md) | Retrieves extended information about the specified console screen buffer. |
| [GetConsoleSelectionInfo function](..\wincon\nf-wincon-getconsoleselectioninfo.md) | Retrieves information about the current console selection. |
| [GetConsoleTitleA function](..\wincon\nf-wincon-getconsoletitlea.md) | Retrieves the title for the current console window. |
| [GetConsoleTitleW function](..\wincon\nf-wincon-getconsoletitlew.md) | Retrieves the title for the current console window. |
| [GetConsoleWindow function](..\wincon\nf-wincon-getconsolewindow.md) | Retrieves the window handle used by the console associated with the calling process. |
| [GetCurrentConsoleFont function](..\wincon\nf-wincon-getcurrentconsolefont.md) | Retrieves information about the current console font. |
| [GetCurrentConsoleFontEx function](..\wincon\nf-wincon-getcurrentconsolefontex.md) | Retrieves extended information about the current console font. |
| [GetLargestConsoleWindowSize function](..\wincon\nf-wincon-getlargestconsolewindowsize.md) | Retrieves the size of the largest possible console window, based on the current font and the size of the display. |
| [GetNumberOfConsoleMouseButtons function](..\wincon\nf-wincon-getnumberofconsolemousebuttons.md) | Retrieves the number of buttons on the mouse used by the current console. |
| [PeekConsoleInputW function](..\wincon\nf-wincon-peekconsoleinputw.md) | Reads data from the specified console input buffer without removing it from the buffer. |
| [ReadConsoleOutputA function](..\wincon\nf-wincon-readconsoleoutputa.md) | Reads character and color attribute data from a rectangular block of character cells in a console screen buffer, and the function writes the data to a rectangular block at a specified location in the destination buffer. |
| [ReadConsoleOutputAttribute function](..\wincon\nf-wincon-readconsoleoutputattribute.md) | Copies a specified number of character attributes from consecutive cells of a console screen buffer, beginning at a specified location. |
| [ReadConsoleOutputCharacterA function](..\wincon\nf-wincon-readconsoleoutputcharactera.md) | Copies a number of characters from consecutive cells of a console screen buffer, beginning at a specified location. |
| [ReadConsoleOutputCharacterW function](..\wincon\nf-wincon-readconsoleoutputcharacterw.md) | Copies a number of characters from consecutive cells of a console screen buffer, beginning at a specified location. |
| [ReadConsoleOutputW function](..\wincon\nf-wincon-readconsoleoutputw.md) | Reads character and color attribute data from a rectangular block of character cells in a console screen buffer, and the function writes the data to a rectangular block at a specified location in the destination buffer. |
| [ScrollConsoleScreenBufferA function](..\wincon\nf-wincon-scrollconsolescreenbuffera.md) | Moves a block of data in a screen buffer. |
| [ScrollConsoleScreenBufferW function](..\wincon\nf-wincon-scrollconsolescreenbufferw.md) | Moves a block of data in a screen buffer. |
| [SetConsoleActiveScreenBuffer function](..\wincon\nf-wincon-setconsoleactivescreenbuffer.md) | Sets the specified screen buffer to be the currently displayed console screen buffer. |
| [SetConsoleCP function](..\wincon\nf-wincon-setconsolecp.md) | Sets the input code page used by the console associated with the calling process. |
| [SetConsoleCursorInfo function](..\wincon\nf-wincon-setconsolecursorinfo.md) | Sets the size and visibility of the cursor for the specified console screen buffer. |
| [SetConsoleCursorPosition function](..\wincon\nf-wincon-setconsolecursorposition.md) | Sets the cursor position in the specified console screen buffer. |
| [SetConsoleDisplayMode function](..\wincon\nf-wincon-setconsoledisplaymode.md) | Sets the display mode of the specified console screen buffer. |
| [SetConsoleHistoryInfo function](..\wincon\nf-wincon-setconsolehistoryinfo.md) | Sets the history settings for the calling process's console. |
| [SetConsoleOutputCP function](..\wincon\nf-wincon-setconsoleoutputcp.md) | Sets the output code page used by the console associated with the calling process. |
| [SetConsoleScreenBufferInfoEx function](..\wincon\nf-wincon-setconsolescreenbufferinfoex.md) | Sets extended information about the specified console screen buffer. |
| [SetConsoleScreenBufferSize function](..\wincon\nf-wincon-setconsolescreenbuffersize.md) | Changes the size of the specified console screen buffer. |
| [SetConsoleTextAttribute function](..\wincon\nf-wincon-setconsoletextattribute.md) | Sets the attributes of characters written to the console screen buffer by the WriteFile or WriteConsole function, or echoed by the ReadFile or ReadConsole function. |
| [SetConsoleTitleA function](..\wincon\nf-wincon-setconsoletitlea.md) | Sets the title for the current console window. |
| [SetConsoleTitleW function](..\wincon\nf-wincon-setconsoletitlew.md) | Sets the title for the current console window. |
| [SetConsoleWindowInfo function](..\wincon\nf-wincon-setconsolewindowinfo.md) | Sets the current size and position of a console screen buffer's window. |
| [SetCurrentConsoleFontEx function](..\wincon\nf-wincon-setcurrentconsolefontex.md) | Sets extended information about the current console font. |
| [WriteConsoleInputA function](..\wincon\nf-wincon-writeconsoleinputa.md) | Writes data directly to the console input buffer. |
| [WriteConsoleInputW function](..\wincon\nf-wincon-writeconsoleinputw.md) | Writes data directly to the console input buffer. |
| [WriteConsoleOutputA function](..\wincon\nf-wincon-writeconsoleoutputa.md) | Writes character and color attribute data to a specified rectangular block of character cells in a console screen buffer. |
| [WriteConsoleOutputAttribute function](..\wincon\nf-wincon-writeconsoleoutputattribute.md) | Copies a number of character attributes to consecutive cells of a console screen buffer, beginning at a specified location. |
| [WriteConsoleOutputCharacterA function](..\wincon\nf-wincon-writeconsoleoutputcharactera.md) | Copies a number of characters to consecutive cells of a console screen buffer, beginning at a specified location. |
| [WriteConsoleOutputCharacterW function](..\wincon\nf-wincon-writeconsoleoutputcharacterw.md) | Copies a number of characters to consecutive cells of a console screen buffer, beginning at a specified location. |
| [WriteConsoleOutputW function](..\wincon\nf-wincon-writeconsoleoutputw.md) | Writes character and color attribute data to a specified rectangular block of character cells in a console screen buffer. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [PHANDLER_ROUTINE callback](..\wincon\nc-wincon-phandler_routine.md) | An application-defined function used with the SetConsoleCtrlHandler function. A console process uses this function to handle control signals received by the process. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_CHAR_INFO structure](..\wincon\ns-wincon-_char_info.md) | Specifies a Unicode or ANSI character and its attributes. This structure is used by console functions to read from and write to a console screen buffer. |
| [_CONSOLE_CURSOR_INFO structure](..\wincon\ns-wincon-_console_cursor_info.md) | Contains information about the console cursor. |
| [_CONSOLE_FONT_INFO structure](..\wincon\ns-wincon-_console_font_info.md) | Contains information for a console font. |
| [_CONSOLE_FONT_INFOEX structure](..\wincon\ns-wincon-_console_font_infoex.md) | Contains extended information for a console font. |
| [_CONSOLE_HISTORY_INFO structure](..\wincon\ns-wincon-_console_history_info.md) | Contains information about the console history. |
| [_CONSOLE_READCONSOLE_CONTROL structure](..\wincon\ns-wincon-_console_readconsole_control.md) | Contains information for a console read operation. |
| [_CONSOLE_SCREEN_BUFFER_INFO structure](..\wincon\ns-wincon-_console_screen_buffer_info.md) | Contains information about a console screen buffer. |
| [_CONSOLE_SCREEN_BUFFER_INFOEX structure](..\wincon\ns-wincon-_console_screen_buffer_infoex.md) | Contains extended information about a console screen buffer. |
| [_CONSOLE_SELECTION_INFO structure](..\wincon\ns-wincon-_console_selection_info.md) | Contains information for a console selection. |
| [_COORD structure](..\wincon\ns-wincon-_coord.md) | Defines the coordinates of a character cell in a console screen buffer. |
| [_FOCUS_EVENT_RECORD structure](..\wincon\ns-wincon-_focus_event_record.md) | Describes a focus event in a console INPUT_RECORD structure. These events are used internally and should be ignored. |
| [_INPUT_RECORD structure](..\wincon\ns-wincon-_input_record.md) | Describes an input event in the console input buffer. |
| [_KEY_EVENT_RECORD structure](..\wincon\ns-wincon-_key_event_record.md) | Describes a keyboard input event in a console INPUT_RECORD structure. |
| [_MENU_EVENT_RECORD structure](..\wincon\ns-wincon-_menu_event_record.md) | Describes a menu event in a console INPUT_RECORD structure. These events are used internally and should be ignored. |
| [_MOUSE_EVENT_RECORD structure](..\wincon\ns-wincon-_mouse_event_record.md) | Describes a mouse input event in a console INPUT_RECORD structure. |
| [_SMALL_RECT structure](..\wincon\ns-wincon-_small_rect.md) | Defines the coordinates of the upper left and lower right corners of a rectangle. |
| [_WINDOW_BUFFER_SIZE_RECORD structure](..\wincon\ns-wincon-_window_buffer_size_record.md) | Describes a change in the size of the console screen buffer. |
