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

# GetUpdatedClipboardFormats function


## -description


Retrieves the currently supported clipboard formats.


## -parameters




### -param lpuiFormats [out]

Type: <b>PUINT</b>

An array of clipboard formats. For a description of the standard clipboard formats, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a>.


### -param cFormats [in]

Type: <b>UINT</b>

The number of entries in the array pointed to by <i>lpuiFormats</i>.


### -param pcFormatsOut [out]

Type: <b>PUINT</b>

The actual number of clipboard formats in the array pointed to by <i>lpuiFormats</i>.


## -returns



Type: <b>BOOL</b>

The function returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional details.



