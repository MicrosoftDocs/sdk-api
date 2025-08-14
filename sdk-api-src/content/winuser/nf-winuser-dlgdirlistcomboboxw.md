---
UID: NF:winuser.DlgDirListComboBoxW
title: DlgDirListComboBoxW function (winuser.h)
description: Replaces the contents of a combo box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list of names can include mapped drive letters. (Unicode)
helpviewer_keywords: ["DDL_ARCHIVE", "DDL_DIRECTORY", "DDL_DRIVES", "DDL_EXCLUSIVE", "DDL_HIDDEN", "DDL_POSTMSGS", "DDL_READONLY", "DDL_READWRITE", "DDL_SYSTEM", "DlgDirListComboBox", "DlgDirListComboBox function [Windows Controls]", "DlgDirListComboBoxW", "_win32_DlgDirListComboBox", "_win32_DlgDirListComboBox_cpp", "controls.DlgDirListComboBox", "controls._win32_DlgDirListComboBox", "winuser/DlgDirListComboBox", "winuser/DlgDirListComboBoxW"]
old-location: controls\DlgDirListComboBox.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxfunctions\dlgdirlistcombobox.htm
ms.date: 12/05/2018
ms.keywords: DDL_ARCHIVE, DDL_DIRECTORY, DDL_DRIVES, DDL_EXCLUSIVE, DDL_HIDDEN, DDL_POSTMSGS, DDL_READONLY, DDL_READWRITE, DDL_SYSTEM, DlgDirListComboBox, DlgDirListComboBox function [Windows Controls], DlgDirListComboBoxA, DlgDirListComboBoxW, _win32_DlgDirListComboBox, _win32_DlgDirListComboBox_cpp, controls.DlgDirListComboBox, controls._win32_DlgDirListComboBox, winuser/DlgDirListComboBox, winuser/DlgDirListComboBoxA, winuser/DlgDirListComboBoxW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DlgDirListComboBoxW (Unicode) and DlgDirListComboBoxA (ANSI)
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
 - DlgDirListComboBoxW
 - winuser/DlgDirListComboBoxW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-0.dll
 - User32.dll
api_name:
 - DlgDirListComboBox
 - DlgDirListComboBoxA
 - DlgDirListComboBoxW
---

# DlgDirListComboBoxW function


## -description

Replaces the contents of a combo box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list of names can include mapped drive letters.

## -parameters

### -param hDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the combo box.

### -param lpPathSpec [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer containing a null-terminated string that specifies an absolute path, relative path, or file name. An absolute path can begin with a drive letter (for example, d:\\) or a UNC name (for example, &#92;&#92;<i>machinename</i>&#92;<i>sharename</i>). 
        
                    

The function splits the string into a directory and a file name. The function searches the directory for names that match the file name. If the string does not specify a directory, the function searches the current directory. 

If the string includes a file name, the file name must contain at least one wildcard character (? or *). If the string does not include a file name, the function behaves as if you had specified the asterisk wildcard character (*) as the file name. All names in the specified directory that match the file name and have the attributes specified by the <i>uFiletype</i> parameter are added to the list displayed in the combo box.

### -param nIDComboBox [in]

Type: <b>int</b>

The identifier of a combo box in the <i>hDlg</i> dialog box. If this parameter is zero, <b>DlgDirListComboBox</b> does not try to fill a combo box.

### -param nIDStaticPath [in]

Type: <b>int</b>

The identifier of a static control in the <i>hDlg</i> dialog box. <b>DlgDirListComboBox</b> sets the text of this control to display the current drive and directory. This parameter can be zero if you do not want to display the current drive and directory.

### -param uFiletype [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A set of bit flags that specifies the attributes of the files or directories to be added to the combo box. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DDL_ARCHIVE"></a><a id="ddl_archive"></a><dl>
<dt><b>DDL_ARCHIVE</b></dt>
</dl>
</td>
<td width="60%">
Includes archived files.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_DIRECTORY"></a><a id="ddl_directory"></a><dl>
<dt><b>DDL_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
Includes subdirectories, which are enclosed in square brackets ([ ]).

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_DRIVES"></a><a id="ddl_drives"></a><dl>
<dt><b>DDL_DRIVES</b></dt>
</dl>
</td>
<td width="60%">
All mapped drives are added to the list. Drives are listed in the form [-<i>x</i>-], where <i>x</i> is the drive letter.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_EXCLUSIVE"></a><a id="ddl_exclusive"></a><dl>
<dt><b>DDL_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
Includes only files with the specified attributes. By default, read/write files are listed even if DDL_READWRITE is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_HIDDEN"></a><a id="ddl_hidden"></a><dl>
<dt><b>DDL_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
Includes hidden files.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_READONLY"></a><a id="ddl_readonly"></a><dl>
<dt><b>DDL_READONLY</b></dt>
</dl>
</td>
<td width="60%">
Includes read-only files.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_READWRITE"></a><a id="ddl_readwrite"></a><dl>
<dt><b>DDL_READWRITE</b></dt>
</dl>
</td>
<td width="60%">
Includes read/write files with no additional attributes. This is the default setting.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_SYSTEM"></a><a id="ddl_system"></a><dl>
<dt><b>DDL_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
Includes system files.

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_POSTMSGS"></a><a id="ddl_postmsgs"></a><dl>
<dt><b>DDL_POSTMSGS</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, <b>DlgDirListComboBox</b> uses the <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function to send messages to the combo box. If this flag is not set, <b>DlgDirListComboBox</b> uses the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the function succeeds, the return value is nonzero.
                    
                    

If the function fails, the return value is zero. For example, if the string specified by <i>lpPathSpec</i> is not a valid path, the function fails. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>lpPathSpec</i> specifies a directory, <b>DlgDirListComboBox</b> changes the current directory to the specified directory before filling the combo box. The text of the static control identified by the <i>nIDStaticPath</i> parameter is set to the name of the new current directory. 


<b>DlgDirListComboBox</b> sends the <a href="/windows/desktop/Controls/cb-resetcontent">CB_RESETCONTENT</a> and <a href="/windows/desktop/Controls/cb-dir">CB_DIR</a> messages to the combo box. 

Microsoft Windows NT 4.0 and later: If <i>uFiletype</i> includes the DDL_DIRECTORY flag and <i>lpPathSpec</i> specifies a first-level directory, such as C:\TEMP, the combo box will always include a ".." entry for the root directory. This is true even if the root directory has hidden or system attributes and the DDL_HIDDEN and DDL_SYSTEM flags are not specified. The root directory of an NTFS volume has hidden and system attributes. 

<b>Security Warning:  </b>Using this function incorrectly might compromise the security of your program. Incorrect use of this function includes having <i>lpPathSpec</i> indicate a non-writable buffer, or a buffer without a null-termination. You should review the <a href="/windows/desktop/Controls/sec-comctls">Security Considerations: Microsoft Windows Controls</a> before continuing.

Microsoft Windows NT 4.0 and later: The list displays long file names, if any.

Windows 95 or later: The list displays short file names (the 8.3 form). You can use the <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> functions to get the corresponding long file name.


Windows 95 or later: <b>DlgDirListComboBoxW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="/archive/msdn-magazine/2001/october/mslu-develop-unicode-applications-for-windows-9x-platforms-with-the-microsoft-layer-for-unicode">Microsoft Layer for Unicode on Windows Me/98/95 Systems</a>.




> [!NOTE]
> The winuser.h header defines DlgDirListComboBox as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlista">DlgDirList</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirselectcomboboxexa">DlgDirSelectComboBoxEx</a>



<b>Reference</b>
