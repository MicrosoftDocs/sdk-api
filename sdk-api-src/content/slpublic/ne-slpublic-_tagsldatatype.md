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

# _tagSLDATATYPE enumeration


## -description


Specifies the data type of the buffer returned by the <a href="https://msdn.microsoft.com/007b3f3a-c320-4bbc-ab5c-746b513cb815">SLGetWindowsInformation</a> function.


## -enum-fields




### -field SL_DATA_NONE

The buffer has no data type.


### -field SL_DATA_SZ

The buffer contains a null-terminated Unicode string.


### -field SL_DATA_DWORD

The buffer contains a <b>DWORD</b> value.


### -field SL_DATA_BINARY

The buffer contains a binary value.


### -field SL_DATA_MULTI_SZ

The buffer contains multiple null-terminated Unicode strings.


### -field SL_DATA_SUM

The buffer contains a sum.

