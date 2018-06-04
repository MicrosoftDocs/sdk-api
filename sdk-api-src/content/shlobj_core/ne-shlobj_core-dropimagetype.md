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

# DROPIMAGETYPE enumeration


## -description


Values used with the <a href="https://msdn.microsoft.com/78757001-cac8-412d-a6c3-74bae6eb3ad8">DROPDESCRIPTION</a> structure to specify the drop image.


## -enum-fields




### -field DROPIMAGE_INVALID

No drop image preference; use the default image.


### -field DROPIMAGE_NONE

A red bisected circle such as that found on a "no smoking" sign.


### -field DROPIMAGE_COPY

A plus sign (+) that indicates a copy operation.


### -field DROPIMAGE_MOVE

An arrow that indicates a move operation.


### -field DROPIMAGE_LINK

An arrow that indicates a link.


### -field DROPIMAGE_LABEL

A tag icon that indicates that the metadata will be changed.


### -field DROPIMAGE_WARNING

A yellow exclamation mark that indicates that a problem has been encountered in the operation.


### -field DROPIMAGE_NOIMAGE

<b>Windows 7 and later</b>. Use no drop image.

