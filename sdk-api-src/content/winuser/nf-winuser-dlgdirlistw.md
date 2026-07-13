---
UID: NF:winuser.DlgDirListW
title: DlgDirListW function (winuser.h)
description: Replaces the contents of a list box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list can optionally include mapped drives. (Unicode)
helpviewer_keywords: ["DDL_ARCHIVE", "DDL_DIRECTORY", "DDL_DRIVES", "DDL_EXCLUSIVE", "DDL_HIDDEN", "DDL_POSTMSGS", "DDL_READONLY", "DDL_READWRITE", "DDL_SYSTEM", "DlgDirList", "DlgDirList function [Windows Controls]", "DlgDirListW", "_win32_DlgDirList", "_win32_DlgDirList_cpp", "controls.DlgDirList", "controls._win32_DlgDirList", "winuser/DlgDirList", "winuser/DlgDirListW"]
old-location: controls\DlgDirList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\dlgdirlist.htm
ms.date: 12/05/2018
ms.keywords: DDL_ARCHIVE, DDL_DIRECTORY, DDL_DRIVES, DDL_EXCLUSIVE, DDL_HIDDEN, DDL_POSTMSGS, DDL_READONLY, DDL_READWRITE, DDL_SYSTEM, DlgDirList, DlgDirList function [Windows Controls], DlgDirListA, DlgDirListW, _win32_DlgDirList, _win32_DlgDirList_cpp, controls.DlgDirList, controls._win32_DlgDirList, winuser/DlgDirList, winuser/DlgDirListA, winuser/DlgDirListW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DlgDirListW (Unicode) and DlgDirListA (ANSI)
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
 - DlgDirListW
 - winuser/DlgDirListW
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
 - DlgDirList
 - DlgDirListA
 - DlgDirListW
---

# DlgDirListW function


## -description

Replaces the contents of a list box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list can optionally include mapped drives.

## -parameters

### -param hDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the list box.

### -param lpPathSpec [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer containing a null-terminated string that specifies an absolute path, relative path, or filename. An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\
					<i>machinename</i>\
					<i>sharename</i>). 

The function splits the string into a directory and a filename. The function searches the directory for names that match the filename. If the string does not specify a directory, the function searches the current directory. 

If the string includes a filename, the filename must contain at least one wildcard character (? or *). If the string does not include a filename, the function behaves as if you had specified the asterisk wildcard character (*) as the filename. All names in the specified directory that match the filename and have the attributes specified by the 
						<i>uFileType</i> parameter are added to the list box.

### -param nIDListBox [in]

Type: <b>int</b>

The identifier of a list box in the 
					<i>hDlg</i> dialog box. If this parameter is zero, <b>DlgDirList</b> does not try to fill a list box.

### -param nIDStaticPath [in]

Type: <b>int</b>

The identifier of a static control in the 
					<i>hDlg</i> dialog box. <b>DlgDirList</b> sets the text of this control to display the current drive and directory. This parameter can be zero if you do not want to display the current drive and directory.

### -param uFileType [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the attributes of the files or directories to be added to the list box. This parameter can be one or more of the following values. 

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
Includes subdirectories. Subdirectory names are enclosed in square brackets ([ ]).

</td>
</tr>
<tr>
<td width="40%"><a id="DDL_DRIVES"></a><a id="ddl_drives"></a><dl>
<dt><b>DDL_DRIVES</b></dt>
</dl>
</td>
<td width="60%">
All mapped drives are added to the list. Drives are listed in the form [-
						<i>x</i>-], where 
						<i>x</i> is the drive letter.

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
If set, <b>DlgDirList</b> uses the <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function to send messages to the list box. If not set, <b>DlgDirList</b> uses the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. For example, if the string specified by 
						<i>lpPathSpec</i> is not a valid path, the function fails. To get extended error information, call .

## -remarks

If 
				<i>lpPathSpec</i> specifies a directory, <a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlistcomboboxa">DlgDirListComboBox</a> changes the current directory to the specified directory before filling the list box. The text of the static control identified by the 
				<i>nIDStaticPath</i> parameter is set to the name of the new current directory. 

<b>DlgDirList</b> sends the 
				<a href="/windows/desktop/Controls/lb-resetcontent">LB_RESETCONTENT</a> and 
				<a href="/windows/desktop/Controls/lb-dir">LB_DIR</a> messages to the list box. 

If 
				<i>uFileType</i> includes the DDL_DIRECTORY flag and 
				<i>lpPathSpec</i> specifies a first-level directory, such as C:\TEMP, the list box will always include a ".." entry for the root directory. This is true even if the root directory has hidden or system attributes and the DDL_HIDDEN and DDL_SYSTEM flags are not specified. The root directory of an NTFS volume has hidden and system attributes. 

The directory listing displays long filenames, if any.


#### Examples

For examples, see the following topics: <a href="/windows/desktop/Controls/using-list-boxes">Creating a Directory Listing in a Single-selection List Box</a> and <a href="/windows/desktop/Controls/using-list-boxes">Creating a Multiple-selection List Box</a>. 

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines DlgDirList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirlistcomboboxa">DlgDirListComboBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirselectcomboboxexa">DlgDirSelectComboBoxEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dlgdirselectexa">DlgDirSelectEx</a>



<b>Reference</b>
