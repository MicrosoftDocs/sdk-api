---
UID: NE:spatialaudiometadata.SpatialAudioMetadataWriterOverflowMode
title: SpatialAudioMetadataWriterOverflowMode (spatialaudiometadata.h)
description: Specifies the desired behavior when an ISpatialAudioMetadataWriter attempts to write more items into the metadata buffer than was specified when the client was initialized.
helpviewer_keywords: ["SpatialAudioMetadataWriterOverflowMode","SpatialAudioMetadataWriterOverflowMode enumeration [Core Audio]","SpatialAudioMetadataWriterOverflow_Fail","SpatialAudioMetadataWriterOverflow_MergeWithLast","SpatialAudioMetadataWriterOverflow_MergeWithNew","coreaudio.spatialaudiometadatawriteroverflowmode","spatialaudiometadata/SpatialAudioMetadataWriterOverflowMode","spatialaudiometadata/SpatialAudioMetadataWriterOverflow_Fail","spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithLast","spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithNew"]
old-location: coreaudio\spatialaudiometadatawriteroverflowmode.htm
tech.root: CoreAudio
ms.assetid: B61C8D75-FCC3-42A6-84DE-01DBA7492962
ms.date: 12/05/2018
ms.keywords: SpatialAudioMetadataWriterOverflowMode, SpatialAudioMetadataWriterOverflowMode enumeration [Core Audio], SpatialAudioMetadataWriterOverflow_Fail, SpatialAudioMetadataWriterOverflow_MergeWithLast, SpatialAudioMetadataWriterOverflow_MergeWithNew, coreaudio.spatialaudiometadatawriteroverflowmode, spatialaudiometadata/SpatialAudioMetadataWriterOverflowMode, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_Fail, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithLast, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithNew
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
targetos: Windows
req.typenames: SpatialAudioMetadataWriterOverflowMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioMetadataWriterOverflowMode
 - spatialaudiometadata/SpatialAudioMetadataWriterOverflowMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SpatialAudioMetadata.h
api_name:
 - SpatialAudioMetadataWriterOverflowMode
---

# SpatialAudioMetadataWriterOverflowMode enumeration


## -description

Specifies the desired behavior when an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> attempts to write more items into the metadata buffer than was specified when the client was initialized.

## -enum-fields

### -field SpatialAudioMetadataWriterOverflow_Fail:0

The write operation will fail.

### -field SpatialAudioMetadataWriterOverflow_MergeWithNew

The write operation will succeed, the overflow item will be merged with previous item and adopt the frame offset of newest item.

### -field SpatialAudioMetadataWriterOverflow_MergeWithLast

The write operation will succeed, the overflow item will be merged with previous item and keep the existing frame offset.
