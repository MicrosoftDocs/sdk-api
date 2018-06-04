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

# WICMetadataPattern structure


## -description


Represents a metadata pattern.


## -struct-fields




### -field Position

Type: <b>ULARGE_INTEGER</b>

The position of the pattern.


### -field Length

Type: <b>ULONG</b>

The length of the pattern.


### -field Pattern

Type: <b>BYTE*</b>

Pointer to the pattern.


### -field Mask

Type: <b>BYTE*</b>

Pointer to the pattern mask.


### -field DataOffset

Type: <b>ULARGE_INTEGER</b>

The offset location of the pattern.

