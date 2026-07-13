---
UID: NS:commdlg.tagOFNA
title: OPENFILENAMEA (commdlg.h)
description: Contains information that the GetOpenFileName and GetSaveFileName functions use to initialize an Open or Save As dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. (ANSI)
helpviewer_keywords: ["*LPOPENFILENAMEA","LPOPENFILENAME","LPOPENFILENAME structure pointer [Dialog Boxes]","OFN_ALLOWMULTISELECT","OFN_CREATEPROMPT","OFN_DONTADDTORECENT","OFN_ENABLEHOOK","OFN_ENABLEINCLUDENOTIFY","OFN_ENABLESIZING","OFN_ENABLETEMPLATE","OFN_ENABLETEMPLATEHANDLE","OFN_EXPLORER","OFN_EXTENSIONDIFFERENT","OFN_EX_NOPLACESBAR","OFN_FILEMUSTEXIST","OFN_FORCESHOWHIDDEN","OFN_HIDEREADONLY","OFN_LONGNAMES","OFN_NOCHANGEDIR","OFN_NODEREFERENCELINKS","OFN_NOLONGNAMES","OFN_NONETWORKBUTTON","OFN_NOREADONLYRETURN","OFN_NOTESTFILECREATE","OFN_NOVALIDATE","OFN_OVERWRITEPROMPT","OFN_PATHMUSTEXIST","OFN_READONLY","OFN_SHAREAWARE","OFN_SHOWHELP","OPENFILENAME","OPENFILENAME structure [Dialog Boxes]","OPENFILENAMEA","OPENFILENAMEW","_win32_OPENFILENAME_str","_win32_openfilename_str_cpp","commdlg/LPOPENFILENAME","commdlg/OPENFILENAME","commdlg/OPENFILENAMEA","commdlg/OPENFILENAMEW","dlgbox.openfilename_str","winui._win32_openfilename_str"]
old-location: dlgbox\openfilename_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\openfilename.htm
ms.date: 12/05/2018
ms.keywords: '*LPOPENFILENAMEA, LPOPENFILENAME, LPOPENFILENAME structure pointer [Dialog Boxes], OFN_ALLOWMULTISELECT, OFN_CREATEPROMPT, OFN_DONTADDTORECENT, OFN_ENABLEHOOK, OFN_ENABLEINCLUDENOTIFY, OFN_ENABLESIZING, OFN_ENABLETEMPLATE, OFN_ENABLETEMPLATEHANDLE, OFN_EXPLORER, OFN_EXTENSIONDIFFERENT, OFN_EX_NOPLACESBAR, OFN_FILEMUSTEXIST, OFN_FORCESHOWHIDDEN, OFN_HIDEREADONLY, OFN_LONGNAMES, OFN_NOCHANGEDIR, OFN_NODEREFERENCELINKS, OFN_NOLONGNAMES, OFN_NONETWORKBUTTON, OFN_NOREADONLYRETURN, OFN_NOTESTFILECREATE, OFN_NOVALIDATE, OFN_OVERWRITEPROMPT, OFN_PATHMUSTEXIST, OFN_READONLY, OFN_SHAREAWARE, OFN_SHOWHELP, OPENFILENAME, OPENFILENAME structure [Dialog Boxes], OPENFILENAMEA, OPENFILENAMEW, _win32_OPENFILENAME_str, _win32_openfilename_str_cpp, commdlg/LPOPENFILENAME, commdlg/OPENFILENAME, commdlg/OPENFILENAMEA, commdlg/OPENFILENAMEW, dlgbox.openfilename_str, winui._win32_openfilename_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPENFILENAMEW (Unicode) and OPENFILENAMEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPENFILENAMEA, *LPOPENFILENAMEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFNA
 - commdlg/tagOFNA
 - LPOPENFILENAMEA
 - commdlg/LPOPENFILENAMEA
 - OPENFILENAMEA
 - commdlg/OPENFILENAMEA
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
 - OPENFILENAME
 - OPENFILENAMEA
 - OPENFILENAMEW
---

# OPENFILENAMEA structure


## -description

<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="/windows/win32/shell/common-file-dialog">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Contains information that the <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> functions use to initialize an <b>Open</b> or <b>Save As</b> dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The length, in bytes, of the structure. 
                     Use <code>sizeof (OPENFILENAME)</code> for this parameter.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>OFN_ENABLETEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to a memory object containing a dialog box template. If the <b>OFN_ENABLETEMPLATE</b> flag is set, <b>hInstance</b> is a handle to a module that contains a dialog box template named by the <b>lpTemplateName</b> member. If neither flag is set, this member is ignored. If the <b>OFN_EXPLORER</b> flag is set, the system uses the specified template to create a dialog box that is a child of the default Explorer-style dialog box. If the <b>OFN_EXPLORER</b> flag is not set, the system uses the template to create an old-style dialog box that replaces the default dialog box.

### -field lpstrFilter

Type: <b>LPCTSTR</b>

A buffer containing pairs of null-terminated filter strings. The last string in the buffer must be terminated by two <b>NULL</b> characters. 

The first string in each pair is a display string that describes the filter (for example, "Text Files"), and the second string specifies the filter pattern (for example, <code>"*.TXT"</code>). To specify multiple filter patterns for a single display string, use a semicolon to separate the patterns (for example, <code>"*.TXT;*.DOC;*.BAK"</code>). A pattern string can be a combination of valid file name characters and the asterisk (\*) wildcard character. Do not include spaces in the pattern string.

The system does not change the order of the filters. It displays them in the <b>File Types</b> combo box in the order specified in <b>lpstrFilter</b>.

If <b>lpstrFilter</b> is <b>NULL</b>, the dialog box does not display any filters.

 In the case of a shortcut, if no filter is set, <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> retrieve the name of the .lnk file, not its target. This behavior is the same as setting the <b>OFN_NODEREFERENCELINKS</b> flag in the <b>Flags</b> member. To retrieve a shortcut's target without filtering, use the string <code>"All Files\0*.*\0\0"</code>.

### -field lpstrCustomFilter

Type: <b>LPTSTR</b>

A static buffer that contains a pair of null-terminated filter strings for preserving the filter pattern chosen by the user. The first string is your display string that describes the custom filter, and the second string is the filter pattern selected by the user. The first time your application creates the dialog box, you specify the first string, which can be any nonempty string. When the user selects a file, the dialog box copies the current filter pattern to the second string. The preserved filter pattern can be one of the patterns specified in the <b>lpstrFilter</b> buffer, or it can be a filter pattern typed by the user. The system uses the strings to initialize the user-defined file filter the next time the dialog box is created. If the <b>nFilterIndex</b> member is zero, the dialog box uses the custom filter. 

If this member is <b>NULL</b>, the dialog box does not preserve user-defined filter patterns.

If this member is not <b>NULL</b>, the value of the <b>nMaxCustFilter</b> member must specify the size, in characters, of the <b>lpstrCustomFilter</b> buffer.

### -field nMaxCustFilter

Type: <b>DWORD</b>

The size, in characters, of the buffer identified by <b>lpstrCustomFilter</b>. This buffer should be at least 40 characters long. This member is ignored if <b>lpstrCustomFilter</b> is <b>NULL</b> or points to a <b>NULL</b> string.

### -field nFilterIndex

Type: <b>DWORD</b>

The index of the currently selected filter in the <b>File Types</b> control. The buffer pointed to by <b>lpstrFilter</b> contains pairs of strings that define the filters. The first pair of strings has an index value of 1, the second pair 2, and so on. An index of zero indicates the custom filter specified by	<b>lpstrCustomFilter</b>. You can specify an index on input to indicate the initial filter description and filter pattern for the dialog box. When the user selects a file, <b>nFilterIndex</b> returns the index of the currently displayed filter. If <b>nFilterIndex</b> is zero and <b>lpstrCustomFilter</b> is <b>NULL</b>, the system uses the first filter in the <b>lpstrFilter</b> buffer. If all three members are zero or <b>NULL</b>, the system does not use any filters and does not show any files in the file list control of the dialog box.

### -field lpstrFile

Type: <b>LPTSTR</b>

The file name used to initialize the <b>File Name</b> edit control. The first character of this buffer must be <b>NULL</b> if initialization is not necessary. When the <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> or <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> function returns successfully, this buffer contains the drive designator, path, file name, and extension of the selected file.

If the <b>OFN_ALLOWMULTISELECT</b> flag is set and the user selects multiple files, the buffer contains the current directory followed by the file names of the selected files. For Explorer-style dialog boxes, the directory and file name strings are <b>NULL</b> separated, with an extra <b>NULL</b> character after the last file name. For old-style dialog boxes, the strings are space separated and the function uses short file names for file names with spaces. You can use the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> function to convert between long and short file names. If the user selects only one file, the <b>lpstrFile</b> string does not have a separator between the path and file name.

If the buffer is too small, the function returns <b>FALSE</b> and the <a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a> function returns <b>FNERR_BUFFERTOOSMALL</b>. In this case, the first two bytes of the <b>lpstrFile</b> buffer contain the required size, in bytes or characters.

### -field nMaxFile

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <b>lpstrFile</b>. The buffer must be large enough to store the path and file name string or strings, including the terminating <b>NULL</b> character. The <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> functions return <b>FALSE</b> if the buffer is too small to contain the file information. The buffer should be at least 256 characters long.

### -field lpstrFileTitle

Type: <b>LPTSTR</b>

The file name and extension (without path information) of the selected file. This member can be <b>NULL</b>.

### -field nMaxFileTitle

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <b>lpstrFileTitle</b>. This member is ignored if <b>lpstrFileTitle</b> is <b>NULL</b>.

### -field lpstrInitialDir

Type: <b>LPCTSTR</b>

The initial directory. The algorithm for selecting the initial directory varies on different platforms.

<b>Windows 7:</b>

<ol>
<li>If <b>lpstrInitialDir</b> has the same value as was passed the first time the application used an <b>Open</b> or <b>Save As</b> dialog box, the path most recently selected by the user is used as the initial directory.</li>
<li>Otherwise, if <b>lpstrFile</b> contains a path, that path is the initial directory.</li>
<li>Otherwise, if <b>lpstrInitialDir</b> is not <b>NULL</b>, it specifies the initial directory.</li>
<li>If <b>lpstrInitialDir</b> is <b>NULL</b> and the current directory contains any files of the specified filter types, the initial directory is the current directory.</li>
<li>Otherwise, the initial directory is the personal files directory of the current user.</li>
<li>Otherwise, the initial directory is the Desktop folder.</li>
</ol>
<b>Windows 2000/XP/Vista:</b>

<ol>
<li>If <b>lpstrFile</b> contains a path, that path is the initial directory.</li>
<li>Otherwise, <b>lpstrInitialDir</b> specifies the initial directory.</li>
<li>Otherwise, if the application has used an <b>Open</b> or <b>Save As</b> dialog box in the past, the path most recently used is selected as the initial directory. However, if an application is not run for a long time, its saved selected path is discarded.</li>
<li>If <b>lpstrInitialDir</b> is <b>NULL</b> and the current directory contains any files of the specified filter types, the initial directory is the current directory.</li>
<li>Otherwise, the initial directory is the personal files directory of the current user.</li>
<li>Otherwise, the initial directory is the Desktop folder.</li>
</ol>

### -field lpstrTitle

Type: <b>LPCTSTR</b>

A string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the system uses the default title (that is, <b>Save As</b> or <b>Open</b>).

### -field Flags

Type: <b>DWORD</b>

A set of bit flags you can use to initialize the dialog box. When the dialog box returns, it sets these flags to indicate the user's input. This member can be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OFN_ALLOWMULTISELECT"></a><a id="ofn_allowmultiselect"></a><dl>
<dt><b>OFN_ALLOWMULTISELECT</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The <b>File Name</b> list box allows multiple selections. If you also set the <b>OFN_EXPLORER</b> flag, the dialog box uses the Explorer-style user interface; otherwise, it uses the old-style user interface.

If the user selects more than one file, the <b>lpstrFile</b> buffer returns the path to the current directory followed by the file names of the selected files. The <b>nFileOffset</b> member is the offset, in bytes or characters, to the first file name, and the <b>nFileExtension</b> member is not used. For Explorer-style dialog boxes, the directory and file name strings are <b>NULL</b> separated, with an extra <b>NULL</b> character after the last file name. This format enables the Explorer-style dialog boxes to return long file names that include spaces. For old-style dialog boxes, the directory and file name strings are separated by spaces and the function uses short file names for file names with spaces. You can use the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> function to convert between long and short file names.

If you specify a custom template for an old-style dialog box, the definition of the <b>File Name</b> list box must contain the <b>LBS_EXTENDEDSEL</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_CREATEPROMPT"></a><a id="ofn_createprompt"></a><dl>
<dt><b>OFN_CREATEPROMPT</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
If the user specifies a file that does not exist, this flag causes the dialog box to prompt the user for permission to create the file. If the user chooses to create the file, the dialog box closes and the function returns the specified name; otherwise, the dialog box remains open. If you use this flag with the <b>OFN_ALLOWMULTISELECT</b> flag, the dialog box allows the user to specify only one nonexistent file.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_DONTADDTORECENT"></a><a id="ofn_dontaddtorecent"></a><dl>
<dt><b>OFN_DONTADDTORECENT</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
 Prevents the system from adding a link to the selected file in the file system directory that contains the user's most recently used documents. To retrieve the location of this directory, call the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a> function with the <b>CSIDL_RECENT</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_ENABLEHOOK"></a><a id="ofn_enablehook"></a><dl>
<dt><b>OFN_ENABLEHOOK</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Enables the hook function specified in the <b>lpfnHook</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_ENABLEINCLUDENOTIFY"></a><a id="ofn_enableincludenotify"></a><dl>
<dt><b>OFN_ENABLEINCLUDENOTIFY</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
 Causes the dialog box to send <a href="/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a> notification messages to your <a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a> hook procedure when the user opens a folder. The dialog box sends a notification for each item in the newly opened folder. These messages enable you to control which items the dialog box displays in the folder's item list.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_ENABLESIZING"></a><a id="ofn_enablesizing"></a><dl>
<dt><b>OFN_ENABLESIZING</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
 Enables the Explorer-style dialog box to be resized using either the mouse or the keyboard. By default, the Explorer-style <b>Open</b> and <b>Save As</b> dialog boxes allow the dialog box to be resized regardless of whether this flag is set. This flag is necessary only if you provide a hook procedure or custom template. The old-style dialog box does not permit resizing.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_ENABLETEMPLATE"></a><a id="ofn_enabletemplate"></a><dl>
<dt><b>OFN_ENABLETEMPLATE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The <b>lpTemplateName</b> member is a pointer to the name of a dialog template resource in the module identified by the 
						<b>hInstance</b> member. If the <b>OFN_EXPLORER</b> flag is set, the system uses the specified template to create a dialog box that is a child of the default Explorer-style dialog box. If the <b>OFN_EXPLORER</b> flag is not set, the system uses the template to create an old-style dialog box that replaces the default dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_ENABLETEMPLATEHANDLE"></a><a id="ofn_enabletemplatehandle"></a><dl>
<dt><b>OFN_ENABLETEMPLATEHANDLE</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. The system ignores <b>lpTemplateName</b> if this flag is specified. If the <b>OFN_EXPLORER</b> flag is set, the system uses the specified template to create a dialog box that is a child of the default Explorer-style dialog box. If the <b>OFN_EXPLORER</b> flag is not set, the system uses the template to create an old-style dialog box that replaces the default dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_EXPLORER"></a><a id="ofn_explorer"></a><dl>
<dt><b>OFN_EXPLORER</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Indicates that any customizations made to the <b>Open</b> or <b>Save As</b> dialog box use the Explorer-style customization methods. For more information, see <a href="/windows/desktop/dlgbox/open-and-save-as-dialog-boxes">Explorer-Style Hook Procedures</a> and <a href="/windows/desktop/dlgbox/open-and-save-as-dialog-boxes">Explorer-Style Custom Templates</a>. 

By default, the <b>Open</b> and <b>Save As</b> dialog boxes use the Explorer-style user interface regardless of whether this flag is set. This flag is necessary only if you provide a hook procedure or custom template, or set the <b>OFN_ALLOWMULTISELECT</b> flag.

If you want the old-style user interface, omit the <b>OFN_EXPLORER</b> flag and provide a replacement old-style template or hook procedure. If you want the old style but do not need a custom template or hook procedure, simply provide a hook procedure that always returns <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_EXTENSIONDIFFERENT"></a><a id="ofn_extensiondifferent"></a><dl>
<dt><b>OFN_EXTENSIONDIFFERENT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The user typed a file name extension that differs from the extension specified by <b>lpstrDefExt</b>. The function does not use this flag if <b>lpstrDefExt</b> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_FILEMUSTEXIST"></a><a id="ofn_filemustexist"></a><dl>
<dt><b>OFN_FILEMUSTEXIST</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The user can type only names of existing files in the <b>File Name</b> entry field. If this flag is specified and the user enters an invalid name, the dialog box procedure displays a warning in a message box. If this flag is specified, the <b>OFN_PATHMUSTEXIST</b> flag is also used. This flag can be used in an <b>Open</b> dialog box. It cannot be used with a <b>Save As</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_FORCESHOWHIDDEN"></a><a id="ofn_forceshowhidden"></a><dl>
<dt><b>OFN_FORCESHOWHIDDEN</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
 Forces the showing of system and hidden files, thus overriding the user setting to show or not show hidden files. However, a file that is marked both system and hidden is not shown.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_HIDEREADONLY"></a><a id="ofn_hidereadonly"></a><dl>
<dt><b>OFN_HIDEREADONLY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Hides the <b>Read Only</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_LONGNAMES"></a><a id="ofn_longnames"></a><dl>
<dt><b>OFN_LONGNAMES</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
For old-style dialog boxes, this flag causes the dialog box to use long file names. If this flag is not specified, or if the <b>OFN_ALLOWMULTISELECT</b> flag is also set, old-style dialog boxes use short file names (8.3 format) for file names with spaces. Explorer-style dialog boxes ignore this flag and always display long file names.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NOCHANGEDIR"></a><a id="ofn_nochangedir"></a><dl>
<dt><b>OFN_NOCHANGEDIR</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Restores the current directory to its original value if the user changed the directory while searching for files.

 This flag is ineffective for <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NODEREFERENCELINKS"></a><a id="ofn_nodereferencelinks"></a><dl>
<dt><b>OFN_NODEREFERENCELINKS</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Directs the dialog box to return the path and file name of the selected shortcut (.LNK) file. If this value is not specified, the dialog box returns the path and file name of the file referenced by the shortcut.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NOLONGNAMES"></a><a id="ofn_nolongnames"></a><dl>
<dt><b>OFN_NOLONGNAMES</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
For old-style dialog boxes, this flag causes the dialog box to use short file names (8.3 format). Explorer-style dialog boxes ignore this flag and always display long file names.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NONETWORKBUTTON"></a><a id="ofn_nonetworkbutton"></a><dl>
<dt><b>OFN_NONETWORKBUTTON</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Hides and disables the <b>Network</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NOREADONLYRETURN"></a><a id="ofn_noreadonlyreturn"></a><dl>
<dt><b>OFN_NOREADONLYRETURN</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The returned file does not have the <b>Read Only</b> check box selected and is not in a write-protected directory.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NOTESTFILECREATE"></a><a id="ofn_notestfilecreate"></a><dl>
<dt><b>OFN_NOTESTFILECREATE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The file is not created before the dialog box is closed. This flag should be specified if the application saves the file on a create-nonmodify network share. When an application specifies this flag, the library does not check for write protection, a full disk, an open drive door, or network protection. Applications using this flag must perform file operations carefully, because a file cannot be reopened once it is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_NOVALIDATE"></a><a id="ofn_novalidate"></a><dl>
<dt><b>OFN_NOVALIDATE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The common dialog boxes allow invalid characters in the returned file name. Typically, the calling application uses a hook procedure that checks the file name by using the <a href="/windows/desktop/dlgbox/fileokstring">FILEOKSTRING</a> message. If the text box in the edit control is empty or contains nothing but spaces, the lists of files and directories are updated. If the text box in the edit control contains anything else, <b>nFileOffset</b> and <b>nFileExtension</b> are set to values generated by parsing the text. No default extension is added to the text, nor is text copied to the buffer specified by <b>lpstrFileTitle</b>. If the value specified by <b>nFileOffset</b> is less than zero, the file name is invalid. Otherwise, the file name is valid, and <b>nFileExtension</b> and <b>nFileOffset</b> can be used as if the <b>OFN_NOVALIDATE</b> flag had not been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_OVERWRITEPROMPT"></a><a id="ofn_overwriteprompt"></a><dl>
<dt><b>OFN_OVERWRITEPROMPT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Causes the <b>Save As</b> dialog box to generate a message box if the selected file already exists. The user must confirm whether to overwrite the file.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_PATHMUSTEXIST"></a><a id="ofn_pathmustexist"></a><dl>
<dt><b>OFN_PATHMUSTEXIST</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The user can type only valid paths and file names. If this flag is used and the user types an invalid path and file name in the <b>File Name</b> entry field, the dialog box function displays a warning in a message box.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_READONLY"></a><a id="ofn_readonly"></a><dl>
<dt><b>OFN_READONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes the <b>Read Only</b> check box to be selected initially when the dialog box is created. This flag indicates the state of the <b>Read Only</b> check box when the dialog box is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_SHAREAWARE"></a><a id="ofn_shareaware"></a><dl>
<dt><b>OFN_SHAREAWARE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Specifies that if a call to the  <a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> function fails because of a network sharing violation, the error is ignored and the dialog box returns the selected file name. If this flag is not set, the dialog box notifies your hook procedure when a network sharing violation occurs for the file name specified by the user. If you set the <b>OFN_EXPLORER</b> flag, the dialog box sends the <a href="/windows/desktop/dlgbox/cdn-shareviolation">CDN_SHAREVIOLATION</a> message to the hook procedure. If you do not set <b>OFN_EXPLORER</b>, the dialog box sends the <a href="/windows/desktop/dlgbox/sharevistring">SHAREVISTRING</a> registered message to the hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="OFN_SHOWHELP"></a><a id="ofn_showhelp"></a><dl>
<dt><b>OFN_SHOWHELP</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the <b>Help</b> button. The <b>hwndOwner</b> member must specify the window to receive the <a href="/windows/desktop/dlgbox/helpmsgstring">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button. An Explorer-style dialog box sends a <a href="/windows/desktop/dlgbox/cdn-help">CDN_HELP</a> notification message to your hook procedure when the user clicks the <b>Help</b> button.

</td>
</tr>
</table>

### -field nFileOffset

Type: <b>WORD</b>

The zero-based offset, in characters, from the beginning of the path to the file name in the string pointed to by <b>lpstrFile</b>. For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters. For example, if <b>lpstrFile</b> points to the following string, "c:\dir1\dir2\file.ext", this member contains the value 13 to indicate the offset of the "file.ext" string. If the user selects more than one file, <b>nFileOffset</b> is the offset to the first file name.

### -field nFileExtension

Type: <b>WORD</b>

The zero-based offset, in characters, from the beginning of the path to the file name extension in the string pointed to by <b>lpstrFile</b>. For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters. Usually the file name extension is the substring which follows the last occurrence of the dot (".") character. For example, txt is the extension of the filename readme.txt, html the extension of readme.txt.html. Therefore, if <b>lpstrFile</b> points to the string "c:\dir1\dir2\readme.txt", this member contains the value 20. If <b>lpstrFile</b> points to the string  "c:\dir1\dir2\readme.txt.html", this member contains the value 24. If <b>lpstrFile</b> points to the string  "c:\dir1\dir2\readme.txt.html.", this member contains the value 29. If <b>lpstrFile</b> points to a string that does not contain any "." character such as "c:\dir1\dir2\readme", this member contains zero.

### -field lpstrDefExt

Type: <b>LPCTSTR</b>

The default extension. <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> and <a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> append this extension to the file name if the user fails to type an extension. This string can be any length, but only the first three characters are appended. The string should not contain a period (.). If this member is <b>NULL</b> and the user fails to type an extension, no extension is appended.

### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnHook</b> member. When the system sends the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <b>OPENFILENAME</b> structure specified when the dialog box was created. The hook procedure can use this pointer to get the <b>lCustData</b> value.

### -field lpfnHook

Type: <b>LPOFNHOOKPROC</b>

A pointer to a hook procedure. This member is ignored unless the <b>Flags</b> member includes the <b>OFN_ENABLEHOOK</b> flag.

If the <b>OFN_EXPLORER</b> flag is not set in the <b>Flags</b> member, <b>lpfnHook</b> is a pointer to an <a href="/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)">OFNHookProcOldStyle</a> hook procedure that receives messages intended for the dialog box. The hook procedure returns <b>FALSE</b> to pass a message to the default dialog box procedure or <b>TRUE</b> to discard the message.

If <b>OFN_EXPLORER</b> is set, <b>lpfnHook</b> is a pointer to an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a> hook procedure. The hook procedure receives notification messages sent from the dialog box. The hook procedure also receives messages for any additional controls that you defined by specifying a child dialog template. The hook procedure does not receive messages intended for the standard controls of the default dialog box.

### -field lpTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog template resource in the module identified by the <b>hInstance</b> member. For numbered dialog box resources, this can be a value returned by the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. This member is ignored unless the <b>OFN_ENABLETEMPLATE</b> flag is set in the <b>Flags</b> member. If the <b>OFN_EXPLORER</b> flag is set, the system uses the specified template to create a dialog box that is a child of the default Explorer-style dialog box. If the <b>OFN_EXPLORER</b> flag is not set, the system uses the template to create an old-style dialog box that replaces the default dialog box.

### -field lpEditInfo

This member is conditionally compiled (using `#ifdef _MAC`) so that it is applicable only to Motorola 68K Macintosh computers, and not to Windows client operating systems.

### -field lpstrPrompt

This member is conditionally compiled (using `#ifdef _MAC`) so that it is applicable only to Motorola 68K Macintosh computers, and not to Windows client operating systems.

### -field pvReserved

Type: <b>void*</b>

This member is reserved.

### -field dwReserved

Type: <b>DWORD</b>

This member is reserved.

### -field FlagsEx

Type: <b>DWORD</b>

 A set of bit flags you can use to initialize the dialog box. Currently, this member can be zero or the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OFN_EX_NOPLACESBAR"></a><a id="ofn_ex_noplacesbar"></a><dl>
<dt><b>OFN_EX_NOPLACESBAR</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the places bar is not displayed. If this flag is not set, Explorer-style dialog boxes include a places bar containing icons for commonly-used folders, such as Favorites and Desktop.

</td>
</tr>
</table>

## -remarks

For compatibility reasons, the Places Bar is hidden if <b>Flags</b> is set to <b>OFN_ENABLEHOOK</b> and <b>lStructSize</b> is <b>OPENFILENAME_SIZE_VERSION_400</b>.





> [!NOTE]
> The commdlg.h header defines OPENFILENAME as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a>
