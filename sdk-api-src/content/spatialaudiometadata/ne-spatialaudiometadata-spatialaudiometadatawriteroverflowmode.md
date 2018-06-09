---
UID: NE:spatialaudiometadata.SpatialAudioMetadataWriterOverflowMode
title: SpatialAudioMetadataWriterOverflowMode
author: windows-sdk-content
description: Specifies the desired behavior when an ISpatialAudioMetadataWriter attempts to write more items into the metadata buffer than was specified when the client was initialized.
old-location: coreaudio\spatialaudiometadatawriteroverflowmode.htm
old-project: CoreAudio
ms.assetid: B61C8D75-FCC3-42A6-84DE-01DBA7492962
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SpatialAudioMetadataWriterOverflowMode, SpatialAudioMetadataWriterOverflowMode enumeration [Core Audio], SpatialAudioMetadataWriterOverflow_Fail, SpatialAudioMetadataWriterOverflow_MergeWithLast, SpatialAudioMetadataWriterOverflow_MergeWithNew, coreaudio.spatialaudiometadatawriteroverflowmode, spatialaudiometadata/SpatialAudioMetadataWriterOverflowMode, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_Fail, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithLast, spatialaudiometadata/SpatialAudioMetadataWriterOverflow_MergeWithNew
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SpatialAudioMetadata.h
api_name:
 - SpatialAudioMetadataWriterOverflowMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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

