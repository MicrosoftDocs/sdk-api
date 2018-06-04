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

# SHGetLocalizedName function


## -description


Retrieves the localized name of a file in a Shell folder.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string that specifies the fully qualified path of the file.


### -param pszResModule [out]

Type: <b>PWSTR</b>

When this function returns, contains a pointer to a string resource that specifies the localized version of the file name.


### -param cch

Type: <b>UINT</b>

When this function returns, contains the size of the string, in <b>WCHARs</b>, at <i>pszResModule</i>.


### -param pidsRes [out]

Type: <b>int*</b>

When this function returns, contains a pointer to the ID of the localized file name in the resource file.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



