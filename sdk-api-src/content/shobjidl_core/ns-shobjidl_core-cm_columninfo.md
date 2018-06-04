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

# CM_COLUMNINFO structure


## -description


Defines column information. Used by members of the <a href="https://msdn.microsoft.com/d01cacd8-1867-4f44-bbc3-876bd727c0fe">IColumnManager</a> interface.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.


### -field dwMask

Type: <b>DWORD</b>

One or more values from the <a href="https://msdn.microsoft.com/c6ba9410-7c56-428c-9ad9-4e769c047863">CM_MASK</a> enumeration that specify which members of this structure are valid.


### -field dwState

Type: <b>DWORD</b>

One or more values from the <a href="https://msdn.microsoft.com/a614dfdc-9535-40c4-9a17-5ab032113508">CM_STATE</a> enumeration that specify the state of the column.


### -field uWidth

Type: <b>UINT</b>

One of the members of the <a href="https://msdn.microsoft.com/c5778bcc-fc9e-499a-b5e5-31c4f2df4871">CM_SET_WIDTH_VALUE</a> enumeration that specifies the column width.


### -field uDefaultWidth

Type: <b>UINT</b>

The default width of the column.


### -field uIdealWidth

Type: <b>UINT</b>

The ideal width of the column.


### -field wszName

Type: <b>WCHAR[MAX_COLUMN_NAME_LEN]</b>

A buffer of size MAX_COLUMN_NAME_LEN that contains the name of the column as a null-terminated Unicode string.

