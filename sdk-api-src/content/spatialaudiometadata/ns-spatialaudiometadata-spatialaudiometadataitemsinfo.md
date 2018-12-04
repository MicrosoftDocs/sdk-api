---
UID: NS:spatialaudiometadata.SpatialAudioMetadataItemsInfo
title: SpatialAudioMetadataItemsInfo
author: windows-sdk-content
description: Provides information about an ISpatialAudioMetadataItems object. Get a copy of this structure by calling GetInfo.
old-location: coreaudio\spatialaudiometadataitemsinfo.htm
tech.root: CoreAudio
ms.assetid: EC694B26-988B-4765-8B9F-130FCF614166
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PSpatialAudioMetadataItemsInfo, PSpatialAudioMetadataItemsInfo structure pointer [Core Audio], SpatialAudioMetadataItemsInfo, SpatialAudioMetadataItemsInfo structure [Core Audio], coreaudio.spatialaudiometadataitemsinfo, spatialaudiometadata/PSpatialAudioMetadataItemsInfo, spatialaudiometadata/SpatialAudioMetadataItemsInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SpatialAudioMetadataItemsInfo
req.redist: 
---

# SpatialAudioMetadataItemsInfo structure


## -description


Provides information about an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object. Get a copy of this structure by calling <a href="https://msdn.microsoft.com/F54BF2B9-B9A4-47EF-8C18-DC58B24B617E">GetInfo</a>.


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

 



