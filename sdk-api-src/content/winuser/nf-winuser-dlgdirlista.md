---
UID: NF:winuser.DlgDirListA
title: DlgDirListA function
author: windows-sdk-content
description: Replaces the contents of a list box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list can optionally include mapped drives.
old-location: controls\DlgDirList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\dlgdirlist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DDL_ARCHIVE, DDL_DIRECTORY, DDL_DRIVES, DDL_EXCLUSIVE, DDL_HIDDEN, DDL_POSTMSGS, DDL_READONLY, DDL_READWRITE, DDL_SYSTEM, DlgDirList, DlgDirList function [Windows Controls], DlgDirListA, DlgDirListW, _win32_DlgDirList, _win32_DlgDirList_cpp, controls.DlgDirList, controls._win32_DlgDirList, winuser/DlgDirList, winuser/DlgDirListA, winuser/DlgDirListW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DlgDirList
 - DlgDirListA
 - DlgDirListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DlgDirListA function


## -description


Replaces the contents of a list box with the names of the subdirectories and files in a specified directory. You can filter the list of names by specifying a set of file attributes. The list can optionally include mapped drives.


## -parameters




### -param hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the list box. 


### -param lpPathSpec [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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
If set, <b>DlgDirList</b> uses the <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> function to send messages to the list box. If not set, <b>DlgDirList</b> uses the <a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a> function.

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
				<i>lpPathSpec</i> specifies a directory, <a href="https://msdn.microsoft.com/65b27196-8e85-483d-9965-e7cbc1b09b5e">DlgDirListComboBox</a> changes the current directory to the specified directory before filling the list box. The text of the static control identified by the 
				<i>nIDStaticPath</i> parameter is set to the name of the new current directory. 

<b>DlgDirList</b> sends the 
				<a href="https://msdn.microsoft.com/3865e45e-62da-457a-801c-2f9a61687022">LB_RESETCONTENT</a> and 
				<a href="https://msdn.microsoft.com/5ec134e9-fe42-4cc0-bdea-fa5e66c218f6">LB_DIR</a> messages to the list box. 

If 
				<i>uFileType</i> includes the DDL_DIRECTORY flag and 
				<i>lpPathSpec</i> specifies a first-level directory, such as C:\TEMP, the list box will always include a ".." entry for the root directory. This is true even if the root directory has hidden or system attributes and the DDL_HIDDEN and DDL_SYSTEM flags are not specified. The root directory of an NTFS volume has hidden and system attributes. 

The directory listing displays long filenames, if any.


#### Examples

For examples, see the following topics: <a href="Using_List_Boxes.htm">Creating a Directory Listing in a Single-selection List Box</a> and <a href="Using_List_Boxes.htm">Creating a Multiple-selection List Box</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/65b27196-8e85-483d-9965-e7cbc1b09b5e">DlgDirListComboBox</a>



<a href="https://msdn.microsoft.com/c7b1e071-1e36-4903-8fb1-dab2ee7af519">DlgDirSelectComboBoxEx</a>



<a href="https://msdn.microsoft.com/12d96fb1-fa68-49ed-9f73-b008ca61b709">DlgDirSelectEx</a>



<b>Reference</b>
 

 

