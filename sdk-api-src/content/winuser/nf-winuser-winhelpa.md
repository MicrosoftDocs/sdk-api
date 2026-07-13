---
UID: NF:winuser.WinHelpA
title: WinHelpA function (winuser.h)
description: Launches Windows Help (Winhelp.exe) and passes additional data that indicates the nature of the help requested by the application. (ANSI)
helpviewer_keywords: ["WinHelpA", "winuser/WinHelpA"]
old-location: shell\WinHelp.htm
tech.root: shell
ms.assetid: fce80bac-2a44-46e7-a87a-ef93f4599807
ms.date: 12/05/2018
ms.keywords: WinHelp, WinHelp function [Windows Shell], WinHelpA, WinHelpW, _win32_WinHelp, shell.WinHelp, winuser/WinHelp, winuser/WinHelpA, winuser/WinHelpW
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WinHelpW (Unicode) and WinHelpA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHelpA
 - winuser/WinHelpA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - WinHelp
 - WinHelpA
 - WinHelpW
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# WinHelpA function


## -description

Launches Windows Help (Winhelp.exe) and passes additional data that indicates the nature of the help requested by the application.

## -parameters

### -param hWndMain

Type: <b>HWND</b>

A handle to the window requesting help. The <b>WinHelp</b> function uses this handle to keep track of which applications have requested help. If the <i>uCommand</i> parameter specifies <b>HELP_CONTEXTMENU</b> or <b>HELP_WM_HELP</b>, <i>hWndMain</i> identifies the control requesting help.

### -param lpszHelp

Type: <b>LPCTSTR</b>

The address of a null-terminated string containing the path, if necessary, and the name of the Help file that <b>WinHelp</b> is to display.
	
    				

The file name can be followed by an angle bracket (&gt;) and the name of a secondary window if the topic is to be displayed in a secondary window rather than in the primary window. You must define the name of the secondary window in the [WINDOWS] section of the Help project (.hpj) file.

### -param uCommand

Type: <b>UINT</b>

The type of help requested. For a list of possible values and how they affect the value to place in the <i>dwData</i> parameter, see the Remarks section.

### -param dwData

Type: <b>ULONG_PTR</b>

Additional data. The value used depends on the value of the <i>uCommand</i> parameter. For a list of possible <i>dwData</i> values, see the Remarks section.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before closing the window that requested help, the application must call <b>WinHelp</b> with the <i>uCommand</i> parameter set to HELP_QUIT. Until all applications have done this, Windows Help will not terminate. Note that calling Windows Help with the HELP_QUIT command is not necessary if you used the HELP_CONTEXTPOPUP command to start Windows Help.

This function fails if called from any context but the current user.

The following table shows the possible values for the <i>uCommand</i> parameter and the corresponding formats of the <i>dwData</i> parameter.

<table class="clsStd">
<tr>
<th><i>uCommand</i></th>
<th>Action</th>
<th><i>dwData</i></th>
</tr>
<tr>
<td>HELP_COMMAND</td>
<td>Executes a Help macro or macro string.</td>
<td>Address of a string that specifies the name of the Help macro(s) to run. If the string specifies multiple macro names, the names must be separated by semicolons. You must use the short form of the macro name for some macros because Windows Help does not support the long name.</td>
</tr>
<tr>
<td>HELP_CONTENTS</td>
<td>Displays the topic specified by the Contents option in the [OPTIONS] section of the .hpj file. This command is for backward compatibility. New applications should provide a .cnt file and use the HELP_FINDER command.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_CONTEXT</td>
<td>Displays the topic identified by the specified context identifier defined in the [MAP] section of the .hpj file.</td>
<td>Contains the context identifier for the topic.</td>
</tr>
<tr>
<td>HELP_CONTEXTMENU</td>
<td>Displays the <b>Help</b> menu for the selected window, then displays the topic for the selected control in a pop-up window.</td>
<td>Address of an array of <b>DWORD</b> pairs. The first <b>DWORD</b> in each pair is the control identifier, and the second is the context identifier for the topic. The array must be terminated by a pair of zeros {0,0}. If you do not want to add Help to a particular control, set its context identifier to -1.</td>
</tr>
<tr>
<td>HELP_CONTEXTPOPUP</td>
<td>Displays the topic identified by the specified context identifier defined in the [MAP] section of the .hpj file in a pop-up window.</td>
<td>Contains the context identifier for a topic.</td>
</tr>
<tr>
<td>HELP_FINDER</td>
<td>Displays the Help Topics dialog box.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_FORCEFILE</td>
<td>Ensures that Windows Help is displaying the correct Help file. If the incorrect Help file is being displayed, Windows Help opens the correct one; otherwise, there is no action.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_HELPONHELP</td>
<td>Displays help on how to use Windows Help, if the Winhlp32.hlp file is available.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_INDEX</td>
<td>Displays the topic specified by the Contents option in the [OPTIONS] section of the .hpj file. This command is for backward compatibility. New applications should use the HELP_FINDER command.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_KEY</td>
<td>Displays the topic in the keyword table that matches the specified keyword, if there is an exact match. If there is more than one match, displays the Index with the topics listed in the <b>Topics Found</b> list box.</td>
<td>Address of a keyword string. Multiple keywords must be separated by semicolons.</td>
</tr>
<tr>
<td>HELP_MULTIKEY</td>
<td>Displays the topic specified by a keyword in an alternative keyword table.</td>
<td>Address of a <a href="/windows/desktop/api/winuser/ns-winuser-multikeyhelpa">MULTIKEYHELP</a> structure that specifies a table footnote character and a keyword.</td>
</tr>
<tr>
<td>HELP_PARTIALKEY</td>
<td>Displays the topic in the keyword table that matches the specified keyword, if there is an exact match. If there is more than one match, displays the <b>Topics Found</b> dialog box. To display the index without passing a keyword, use a pointer to an empty string.</td>
<td>Address of a keyword string. Multiple keywords must be separated by semicolons.</td>
</tr>
<tr>
<td>HELP_QUIT</td>
<td>Informs Windows Help that it is no longer needed. If no other applications have asked for help, Windows closes Windows Help.</td>
<td>Ignored; set to 0.</td>
</tr>
<tr>
<td>HELP_SETCONTENTS</td>
<td>Specifies the Contents topic. Windows Help displays this topic when the user clicks the <b>Contents</b> button if the Help file does not have an associated .cnt file.</td>
<td>Contains the context identifier for the Contents topic.</td>
</tr>
<tr>
<td>HELP_SETPOPUP_POS</td>
<td>Sets the position of the subsequent pop-up window.</td>
<td>Contains the position data. Use <a href="/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)">MAKELONG</a> to concatenate the horizontal and vertical coordinates into a single value. The pop-up window is positioned as if the mouse cursor were at the specified point when the pop-up window was invoked.</td>
</tr>
<tr>
<td>HELP_SETWINPOS</td>
<td>Displays the Windows Help window, if it is minimized or in memory, and sets its size and position as specified.</td>
<td>Address of a <a href="/windows/desktop/api/winuser/ns-winuser-helpwininfoa">HELPWININFO</a> structure that specifies the size and position of either a primary or secondary Help window.</td>
</tr>
<tr>
<td>HELP_TCARD</td>
<td>Indicates that a command is for a training card instance of Windows Help. Combine this command with other commands using the bitwise OR operator.</td>
<td>Depends on the command with which this command is combined.</td>
</tr>
<tr>
<td>HELP_WM_HELP</td>
<td>Displays the topic for the control identified by the <i>hWndMain</i> parameter in a pop-up window.</td>
<td>Address of an array of <b>DWORD</b> pairs. The first <b>DWORD</b> in each pair is a control identifier, and the second is a context identifier for a topic. The array must be terminated by a pair of zeros {0,0}. If you do not want to add Help to a particular control, set its context identifier to -1.</td>
</tr>
</table>
 





> [!NOTE]
> The winuser.h header defines WinHelp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-helpwininfoa">HELPWININFO</a>



<a href="/windows/desktop/api/winuser/ns-winuser-multikeyhelpa">MULTIKEYHELP</a>
