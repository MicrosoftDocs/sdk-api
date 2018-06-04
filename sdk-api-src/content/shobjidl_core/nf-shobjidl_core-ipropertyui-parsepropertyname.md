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

# IPropertyUI::ParsePropertyName


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Reads the characters of the specified property name and identifies the FMTID and PROPID of the property.


## -parameters




### -param pszName [in]

Type: <b>LPWSTR</b>

A string specifying the property name to parse.


### -param pfmtid [out]

Type: <b>FMTID*</b>

The FMTID of the parsed property.


### -param ppid [out]

Type: <b>PROPID*</b>

The PROPID of the parsed property name.


### -param pchEaten [in, out]

Type: <b>ULONG*</b>

The number of characters that were consumed in parsing <i>pszName</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



