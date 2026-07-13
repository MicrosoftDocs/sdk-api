---
UID: NS:commdlg.tagFINDREPLACEA
title: FINDREPLACEA (commdlg.h)
description: Contains information that the FindText and ReplaceText functions use to initialize the Find and Replace dialog boxes. (ANSI)
helpviewer_keywords: ["*LPFINDREPLACEA","FINDREPLACE","FINDREPLACE structure [Dialog Boxes]","FINDREPLACEA","FINDREPLACEW","FR_DIALOGTERM","FR_DOWN","FR_ENABLEHOOK","FR_ENABLETEMPLATE","FR_ENABLETEMPLATEHANDLE","FR_FINDNEXT","FR_HIDEMATCHCASE","FR_HIDEUPDOWN","FR_HIDEWHOLEWORD","FR_MATCHCASE","FR_NOMATCHCASE","FR_NOUPDOWN","FR_NOWHOLEWORD","FR_REPLACE","FR_REPLACEALL","FR_SHOWHELP","FR_WHOLEWORD","LPFINDREPLACE","LPFINDREPLACE structure pointer [Dialog Boxes]","_win32_FINDREPLACE_str","_win32_findreplace_str_cpp","commdlg/FINDREPLACE","commdlg/FINDREPLACEA","commdlg/FINDREPLACEW","commdlg/LPFINDREPLACE","dlgbox.findreplace_str","winui._win32_findreplace_str"]
old-location: dlgbox\findreplace_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\findreplace.htm
ms.date: 12/05/2018
ms.keywords: '*LPFINDREPLACEA, FINDREPLACE, FINDREPLACE structure [Dialog Boxes], FINDREPLACEA, FINDREPLACEW, FR_DIALOGTERM, FR_DOWN, FR_ENABLEHOOK, FR_ENABLETEMPLATE, FR_ENABLETEMPLATEHANDLE, FR_FINDNEXT, FR_HIDEMATCHCASE, FR_HIDEUPDOWN, FR_HIDEWHOLEWORD, FR_MATCHCASE, FR_NOMATCHCASE, FR_NOUPDOWN, FR_NOWHOLEWORD, FR_REPLACE, FR_REPLACEALL, FR_SHOWHELP, FR_WHOLEWORD, LPFINDREPLACE, LPFINDREPLACE structure pointer [Dialog Boxes], _win32_FINDREPLACE_str, _win32_findreplace_str_cpp, commdlg/FINDREPLACE, commdlg/FINDREPLACEA, commdlg/FINDREPLACEW, commdlg/LPFINDREPLACE, dlgbox.findreplace_str, winui._win32_findreplace_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FINDREPLACEW (Unicode) and FINDREPLACEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FINDREPLACEA, *LPFINDREPLACEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFINDREPLACEA
 - commdlg/tagFINDREPLACEA
 - LPFINDREPLACEA
 - commdlg/LPFINDREPLACEA
 - FINDREPLACEA
 - commdlg/FINDREPLACEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - FINDREPLACE
 - FINDREPLACEA
 - FINDREPLACEW
---

# FINDREPLACEA structure


## -description

Contains information that the <a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a> functions use to initialize the <b>Find</b> and <b>Replace</b> dialog boxes. The <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> registered message uses this structure to pass the user's search or replacement input to the owner window of a <b>Find</b> or <b>Replace</b> dialog box.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The length, in bytes, of the structure.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. The window procedure of the specified window receives <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> messages from the dialog box. This member can be any valid window handle, but it must not be <b>NULL</b>.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>FR_ENABLETEMPLATEHANDLE</b> flag is set in the <b>Flags</b>, <b>hInstance</b> is a handle to a memory object containing a dialog box template. If the <b>FR_ENABLETEMPLATE</b> flag is set, <b>hInstance</b> is a handle to a module that contains a dialog box template named by the <b>lpTemplateName</b> member. If neither flag is set, this member is ignored.

### -field Flags

Type: <b>DWORD</b>

A set of bit flags that you can use to initialize the dialog box. The dialog box sets these flags when it sends the <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> registered message to indicate the user's input. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FR_DIALOGTERM"></a><a id="fr_dialogterm"></a><dl>
<dt><b>FR_DIALOGTERM</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates that the dialog box is closing. When you receive a message with this flag set, the dialog box handle returned by the <a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a> or <a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a> function is no longer valid.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_DOWN"></a><a id="fr_down"></a><dl>
<dt><b>FR_DOWN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If set, the <b>Down</b> button of the direction radio buttons in a <b>Find</b> dialog box is selected indicating that you should search from the current location to the end of the document. If not set, the <b>Up</b> button is selected so you should search to the beginning of the document. You can set this flag to initialize the dialog box. If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates the user's selection.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_ENABLEHOOK"></a><a id="fr_enablehook"></a><dl>
<dt><b>FR_ENABLEHOOK</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Enables the hook function specified in the <b>lpfnHook</b> member. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_ENABLETEMPLATE"></a><a id="fr_enabletemplate"></a><dl>
<dt><b>FR_ENABLETEMPLATE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Indicates that the  <b>hInstance</b> and <b>lpTemplateName</b> members specify a dialog box template to use in place of the default template. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_ENABLETEMPLATEHANDLE"></a><a id="fr_enabletemplatehandle"></a><dl>
<dt><b>FR_ENABLETEMPLATEHANDLE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. The system ignores the <b>lpTemplateName</b> member if this flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_FINDNEXT"></a><a id="fr_findnext"></a><dl>
<dt><b>FR_FINDNEXT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates that the user clicked the <b>Find Next</b> button in a <b>Find</b> or <b>Replace</b> dialog box. The <b>lpstrFindWhat</b> member specifies the string to search for.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_HIDEUPDOWN"></a><a id="fr_hideupdown"></a><dl>
<dt><b>FR_HIDEUPDOWN</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> dialog box, hides the search direction radio buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_HIDEMATCHCASE"></a><a id="fr_hidematchcase"></a><dl>
<dt><b>FR_HIDEMATCHCASE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> or <b>Replace</b> dialog box, hides the <b>Match Case</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_HIDEWHOLEWORD"></a><a id="fr_hidewholeword"></a><dl>
<dt><b>FR_HIDEWHOLEWORD</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> or <b>Replace</b> dialog box, hides the <b>Match Whole Word Only</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_MATCHCASE"></a><a id="fr_matchcase"></a><dl>
<dt><b>FR_MATCHCASE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If set, the <b>Match Case</b> check box is selected indicating that the search should be case-sensitive. If not set, the check box is unselected so the search should be case-insensitive. You can set this flag to initialize the dialog box. If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates the user's selection.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_NOMATCHCASE"></a><a id="fr_nomatchcase"></a><dl>
<dt><b>FR_NOMATCHCASE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> or <b>Replace</b> dialog box, disables the <b>Match Case</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_NOUPDOWN"></a><a id="fr_noupdown"></a><dl>
<dt><b>FR_NOUPDOWN</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> dialog box, disables the search direction radio buttons.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_NOWHOLEWORD"></a><a id="fr_nowholeword"></a><dl>
<dt><b>FR_NOWHOLEWORD</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
If set when initializing a <b>Find</b> or <b>Replace</b> dialog box, disables the <b>Whole Word</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_REPLACE"></a><a id="fr_replace"></a><dl>
<dt><b>FR_REPLACE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates that the user clicked the <b>Replace</b> button in a <b>Replace</b> dialog box. The <b>lpstrFindWhat</b> member specifies the string to be replaced and the <b>lpstrReplaceWith</b> member specifies the replacement string.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_REPLACEALL"></a><a id="fr_replaceall"></a><dl>
<dt><b>FR_REPLACEALL</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates that the user clicked the <b>Replace All</b> button in a <b>Replace</b> dialog box. The <b>lpstrFindWhat</b> member specifies the string to be replaced and the <b>lpstrReplaceWith</b> member specifies the replacement string.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_SHOWHELP"></a><a id="fr_showhelp"></a><dl>
<dt><b>FR_SHOWHELP</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the <b>Help</b> button. The <b>hwndOwner</b> member must specify the window to receive the <a href="/windows/desktop/dlgbox/helpmsgstring">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_WHOLEWORD"></a><a id="fr_wholeword"></a><dl>
<dt><b>FR_WHOLEWORD</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If set, the <b>Match Whole Word Only</b> check box is selected indicating that you should search only for whole words that match the search string. If not set, the check box is unselected so you should also search for word fragments that match the search string. You can set this flag to initialize the dialog box. If set in a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message, indicates the user's selection.

</td>
</tr>
</table>

### -field lpstrFindWhat

Type: <b>LPTSTR</b>

The search string that the user typed in the <b>Find What</b> edit control. You must dynamically allocate the buffer or use a global or static array so it does not go out of scope before the dialog box closes. The buffer should be at least 80 characters long. If the buffer contains a string when you initialize the dialog box, the string is displayed in the <b>Find What</b> edit control. If a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message specifies the <b>FR_FINDNEXT</b> flag, <b>lpstrFindWhat</b> contains the string to search for. The <b>FR_DOWN</b>, <b>FR_WHOLEWORD</b>, and <b>FR_MATCHCASE</b> flags indicate the direction and type of search. If a <b>FINDMSGSTRING</b> message specifies the <b>FR_REPLACE</b> or <b>FR_REPLACE</b> flags, <b>lpstrFindWhat</b> contains the string to be replaced.

### -field lpstrReplaceWith

Type: <b>LPTSTR</b>

The replacement string that the user typed in the <b>Replace With</b> edit control. You must dynamically allocate the buffer or use a global or static array so it does not go out of scope before the dialog box closes. If the buffer contains a string when you initialize the dialog box, the string is displayed in the <b>Replace With</b> edit control.

If a <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message specifies the <b>FR_REPLACE</b> or <b>FR_REPLACEALL</b> flags, <b>lpstrReplaceWith</b> contains the replacement string . 

The <a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a> function ignores this member.

### -field wFindWhatLen

Type: <b>WORD</b>

The length, in bytes, of the buffer pointed to by the <b>lpstrFindWhat</b> member.

### -field wReplaceWithLen

Type: <b>WORD</b>

The length, in bytes, of the buffer pointed to by the <b>lpstrReplaceWith</b> member.

### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnHook</b> member. When the system sends the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <b>FINDREPLACE</b> structure specified when the dialog was created. The hook procedure can use this pointer to get the <b>lCustData</b> value.

### -field lpfnHook

Type: <b>LPFRHOOKPROC</b>

A pointer to an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a> hook procedure that can process messages intended for the dialog box. This member is ignored unless the <b>FR_ENABLEHOOK</b> flag is set in the <b>Flags</b> member. If the hook procedure returns <b>FALSE</b> in response to the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message, the hook procedure must display the dialog box or else the dialog box will not be shown. To do this, first perform any other paint operations, and then call the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> and <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a> functions.

### -field lpTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template is substituted for the standard dialog box template. For numbered dialog box resources, this can be a value returned by the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. This member is ignored unless the <b>FR_ENABLETEMPLATE</b> flag is set in the <b>Flags</b> member.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-findtexta">FindText</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>

## -remarks

> [!NOTE]
> The commdlg.h header defines FINDREPLACE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
