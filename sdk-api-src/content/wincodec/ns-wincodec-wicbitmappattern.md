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

# WICBitmapPattern structure


## -description


Contains members that identify a pattern within an image file which can be used to identify a particular format.


## -struct-fields




### -field Position

Type: <b>ULARGE_INTEGER</b>

The offset the pattern is located in the file.


### -field Length

Type: <b>ULONG</b>

The pattern length.


### -field Pattern

Type: <b>BYTE*</b>

The actual pattern.


### -field Mask

Type: <b>BYTE*</b>

The pattern mask.


### -field EndOfStream

Type: <b>BOOL</b>

The end of the stream.

