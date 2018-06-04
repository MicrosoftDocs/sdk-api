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

# SpatialAudioMetadataCopyMode enumeration


## -description


Specifies the copy mode used when calling <a href="https://msdn.microsoft.com/12ABAD23-7EDF-4F74-AE2E-26C75FA6AB37">ISpatialAudioMetadataCopier::CopyMetadataForFrames</a>.


## -enum-fields




### -field SpatialAudioMetadataCopy_Overwrite

Creates a direct copy of the number of metadata items  specified with the <i>copyFrameCount</i> parameter  into destination buffer, overwriting any previously existing data.


### -field SpatialAudioMetadataCopy_Append

Performs an append operation which will fail if the  resulting <a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a> has too many items.


### -field SpatialAudioMetadataCopy_AppendMergeWithLast

Performs an append operation, and if overflow occurs, extra items are merged into last item, adopting last merged item's offset value.


### -field SpatialAudioMetadataCopy_AppendMergeWithFirst

Performs an append operation, and if overflow occurs, extra items are merged, assigning the offset to the offset of the first non-overflow item.

