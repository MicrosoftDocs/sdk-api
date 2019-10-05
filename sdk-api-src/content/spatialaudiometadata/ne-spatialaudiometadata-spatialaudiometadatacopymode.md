---
UID: NE:spatialaudiometadata.SpatialAudioMetadataCopyMode
title: SpatialAudioMetadataCopyMode (spatialaudiometadata.h)
author: windows-sdk-content
description: Specifies the copy mode used when calling ISpatialAudioMetadataCopier::CopyMetadataForFrames.
old-location: coreaudio\spatialaudiometadatacopymode.htm
tech.root: CoreAudio
ms.assetid: 2E9C2C66-26EB-43E8-A518-25980B287542
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpatialAudioMetadataCopyMode, SpatialAudioMetadataCopy_Append, SpatialAudioMetadataCopy_AppendMergeWithFirst, SpatialAudioMetadataCopy_AppendMergeWithLast, SpatialAudioMetadataCopy_Overwrite, SpatialAudioMetadataWriterCopyMode, SpatialAudioMetadataWriterCopyMode enumeration [Core Audio], coreaudio.spatialaudiometadatacopymode, coreaudio.spatialaudiometadatawritercopymode, spatialaudiometadata/SpatialAudioMetadataCopy_Append, spatialaudiometadata/SpatialAudioMetadataCopy_AppendMergeWithFirst, spatialaudiometadata/SpatialAudioMetadataCopy_AppendMergeWithLast, spatialaudiometadata/SpatialAudioMetadataCopy_Overwrite, spatialaudiometadata/SpatialAudioMetadataWriterCopyMode
ms.topic: enum
f1_keywords: 
 - "spatialaudiometadata/SpatialAudioMetadataWriterCopyMode"
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
 - SpatialAudioMetadataWriterCopyMode
targetos: Windows
req.typenames: SpatialAudioMetadataCopyMode
req.redist: 
ms.custom: 19H1
---

# SpatialAudioMetadataCopyMode enumeration


## -description


Specifies the copy mode used when calling <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-copymetadataforframes">ISpatialAudioMetadataCopier::CopyMetadataForFrames</a>.


## -enum-fields




### -field SpatialAudioMetadataCopy_Overwrite

Creates a direct copy of the number of metadata items  specified with the <i>copyFrameCount</i> parameter  into destination buffer, overwriting any previously existing data.


### -field SpatialAudioMetadataCopy_Append

Performs an append operation which will fail if the  resulting <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a> has too many items.


### -field SpatialAudioMetadataCopy_AppendMergeWithLast

Performs an append operation, and if overflow occurs, extra items are merged into last item, adopting last merged item's offset value.


### -field SpatialAudioMetadataCopy_AppendMergeWithFirst

Performs an append operation, and if overflow occurs, extra items are merged, assigning the offset to the offset of the first non-overflow item.

