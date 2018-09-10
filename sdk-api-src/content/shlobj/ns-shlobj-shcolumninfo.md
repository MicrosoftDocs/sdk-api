---
UID: NS:shlobj.SHCOLUMNINFO
title: SHCOLUMNINFO
author: windows-sdk-content
description: Contains information about the properties of a column. It is used by IColumnProvider::GetColumnInfo.
old-location: shell\SHCOLUMNINFO_str.htm
tech.root: shell
ms.assetid: 6d7caeca-38fe-4477-a278-abf483d8d42c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*LPSHCOLUMNINFO, LPSHCOLUMNINFO, LPSHCOLUMNINFO structure pointer [Windows Shell], SHCOLSTATE_EXTENDED, SHCOLSTATE_HIDDEN, SHCOLSTATE_ONBYDEFAULT, SHCOLSTATE_SECONDARYUI, SHCOLSTATE_SLOW, SHCOLSTATE_TYPE_DATE, SHCOLSTATE_TYPE_INT, SHCOLSTATE_TYPE_STR, SHCOLUMNINFO, SHCOLUMNINFO structure [Windows Shell], _win32_SHCOLUMNINFO_str, shell.SHCOLUMNINFO_str, shlobj/LPSHCOLUMNINFO, shlobj/SHCOLUMNINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - SHCOLUMNINFO
product: Windows
targetos: Windows
req.typenames: SHCOLUMNINFO, *LPSHCOLUMNINFO
req.redist: 
---

# SHCOLUMNINFO structure


## -description


Contains information about the properties of a column. It is used by <a href="https://msdn.microsoft.com/87196252-3835-4828-ad0a-0edcafb286b7">IColumnProvider::GetColumnInfo</a>.


## -struct-fields




### -field scid

Type: <b><a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a></b>

A <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that uniquely identifies the column.


### -field vt

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a></b>

The native <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARIANT</a> type of the column's data.


### -field fmt

Type: <b>DWORD</b>


<a href="https://msdn.microsoft.com/en-us/library/Bb774743(v=VS.85).aspx">List view format</a>. This member is normally set to LVCFMT_LEFT.


### -field cChars

Type: <b>UINT</b>

The default width of the column, in characters.


### -field csFlags

Type: <b>DWORD</b>

Flags indicating the default column state. It can be a combination of the following flags.



#### SHCOLSTATE_TYPE_STR

A string.



#### SHCOLSTATE_TYPE_INT

An integer.



#### SHCOLSTATE_TYPE_DATE

A date.



#### SHCOLSTATE_ONBYDEFAULT

Shown by default in Windows Explorer Details view, even if the user has not selected the column. If this flag is set, the column will be displayed for all folders. There is no way to force a column to be displayed on a per-folder basis.



#### SHCOLSTATE_SLOW

Slow to compute. Windows Explorer should retrieve the data asynchronously and do the computation on a background thread.



#### SHCOLSTATE_EXTENDED

Provided by a handler, not the folder object.



#### SHCOLSTATE_SECONDARYUI

Not displayed in the shortcut menu, but listed in the <b>More...</b> dialog box.



#### SHCOLSTATE_HIDDEN

Not displayed in the user interface.


### -field wszTitle

Type: <b>WCHAR[MAX_COLUMN_NAME_LEN]</b>

A null-terminated Unicode string with the column's title. It must contain no more than MAX_COLUMN_NAME_LEN characters, including the terminating <b>NULL</b>.


### -field wszDescription

Type: <b>WCHAR[MAX_COLUMN_DESC_LEN]</b>

A null-terminated Unicode string with the column's description. It must contain no more than MAX_COLUMN_DESC_LEN characters, including the terminating <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/87196252-3835-4828-ad0a-0edcafb286b7">IColumnProvider::GetColumnInfo</a>
 

 

