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

# FILE_ATTRIBUTES_ARRAY structure


## -description


Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY.


## -struct-fields




### -field cItems

Type: <b>UINT</b>

The number of items in the <b>rgdwFileAttributes</b> array.


### -field dwSumFileAttributes

Type: <b>DWORD</b>

All of the attributes combined using OR.


### -field dwProductFileAttributes

Type: <b>DWORD</b>

All of the attributes combined using AND.


### -field rgdwFileAttributes

Type: <b>DWORD[1]</b>

An array of file attributes.

