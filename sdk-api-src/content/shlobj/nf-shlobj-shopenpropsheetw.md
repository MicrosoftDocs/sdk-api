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

# SHOpenPropSheetW function


## -description


<p class="CCE_Message">[<b>SHOpenPropSheet</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a property sheet from a list of registry keys that contain the <b>CLSID</b>s of the individual sheets, then opens the property sheet.


## -parameters




### -param pszCaption [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a string that contains the caption for the property sheet. This value can be <b>NULL</b> if no caption is needed.


### -param ahkeys [in, optional]

Type: <b>HKEY[]</b>

An array of registry keys that represent the <b>CLSID</b>s of the individual property sheets.


### -param ckeys

Type: <b>UINT</b>

<b>UINT</b> value that specifies the number of property sheets in the array specified by <i>ahkeys</i>.


### -param pclsidDefault

TBD


### -param pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, an OLE object that can be used to carry out actions on the property sheet(s).


### -param psb [in, optional]

Type: <b><a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>*</b>

Not used.


### -param pStartPage [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a string that specifies the start page. This value can be <b>NULL</b>.


#### - pclsidDef [in, optional]

Type: <b>const CLSID*</b>

A pointer to the default <b>CLSID</b>. This value can be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the property sheet was successfully created; otherwise, <b>FALSE</b>.



