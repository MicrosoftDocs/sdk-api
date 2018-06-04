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

# IBrowserService::GetPalette


## -description


Deprecated. Retrieves the browser's palette.


## -parameters




### -param hpal [out]

Type: <b>HPALETTE*</b>

A pointer to the browser's palette handle, if one exists.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_FAIL if there is no palette.




## -remarks



The calling application should not call <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> on the palette handle retrieved in <i>hpal</i>.



