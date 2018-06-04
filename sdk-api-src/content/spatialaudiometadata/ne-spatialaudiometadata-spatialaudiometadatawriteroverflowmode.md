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

# SpatialAudioMetadataWriterOverflowMode enumeration


## -description


Specifies the desired behavior when an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> attempts to write more items into the metadata buffer than was specified when the client was initialized.


## -enum-fields




### -field SpatialAudioMetadataWriterOverflow_Fail

The write operation will fail.


### -field SpatialAudioMetadataWriterOverflow_MergeWithNew

The write operation will succeed, the overflow item will be merged with previous item and adopt the frame offset of newest item.


### -field SpatialAudioMetadataWriterOverflow_MergeWithLast

The write operation will succeed, the overflow item will be merged with previous item and keep the existing frame offset.

