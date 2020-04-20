---
UID: NS:spatialaudiometadata.SpatialAudioMetadataItemsInfo
title: SpatialAudioMetadataItemsInfo (spatialaudiometadata.h)
description: Provides information about an ISpatialAudioMetadataItems object. Get a copy of this structure by calling GetInfo.helpviewer_keywords: ["PSpatialAudioMetadataItemsInfo","PSpatialAudioMetadataItemsInfo structure pointer [Core Audio]","SpatialAudioMetadataItemsInfo","SpatialAudioMetadataItemsInfo structure [Core Audio]","coreaudio.spatialaudiometadataitemsinfo","spatialaudiometadata/PSpatialAudioMetadataItemsInfo","spatialaudiometadata/SpatialAudioMetadataItemsInfo"]
old-location: coreaudio\spatialaudiometadataitemsinfo.htm
tech.root: CoreAudio
ms.assetid: EC694B26-988B-4765-8B9F-130FCF614166
ms.date: 12/05/2018
ms.keywords: PSpatialAudioMetadataItemsInfo, PSpatialAudioMetadataItemsInfo structure pointer [Core Audio], SpatialAudioMetadataItemsInfo, SpatialAudioMetadataItemsInfo structure [Core Audio], coreaudio.spatialaudiometadataitemsinfo, spatialaudiometadata/PSpatialAudioMetadataItemsInfo, spatialaudiometadata/SpatialAudioMetadataItemsInfo
f1_keywords:
- spatialaudiometadata/SpatialAudioMetadataItemsInfo
dev_langs:
- c++
req.header: spatialaudiometadata.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- SpatialAudioMetadata.h
api_name:
- SpatialAudioMetadataItemsInfo
targetos: Windows
req.typenames: SpatialAudioMetadataItemsInfo
req.redist: 
ms.custom: 19H1
---

# SpatialAudioMetadataItemsInfo structure


## -description


Provides information about an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object. Get a copy of this structure by calling <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getinfo">GetInfo</a>.


## -struct-fields




### -field FrameCount

The total frame count, which defines valid item offsets.


### -field ItemCount

The current number of items stored.



#### MaxItemCount

The maximum number of items allowed.



##### MaxValueBufferLength

The size of the largest command value defined by the metadata format.


### -field MaxItemCount

 


### -field MaxValueBufferLength

 



