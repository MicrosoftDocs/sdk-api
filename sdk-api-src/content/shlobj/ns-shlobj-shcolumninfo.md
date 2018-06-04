---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHCOLUMNINFO structure


## -description


Contains information about the properties of a column. It is used by <a href="https://msdn.microsoft.com/87196252-3835-4828-ad0a-0edcafb286b7">IColumnProvider::GetColumnInfo</a>.


## -struct-fields




### -field scid

Type: <b><a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a></b>

A <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that uniquely identifies the column.


### -field vt

Type: <b><a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a></b>

The native <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> type of the column's data.


### -field fmt

Type: <b>DWORD</b>


<a href="https://msdn.microsoft.com/6ffa287d-0284-43c9-80ff-b9c90a83e855">List view format</a>. This member is normally set to LVCFMT_LEFT.


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
 

 

