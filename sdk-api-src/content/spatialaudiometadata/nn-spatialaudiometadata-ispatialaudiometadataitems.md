---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataItems
title: ISpatialAudioMetadataItems (spatialaudiometadata.h)
description: Represents a buffer of spatial audio metadata items.
helpviewer_keywords: ["ISpatialAudioMetadataItems","ISpatialAudioMetadataItems interface [Core Audio]","ISpatialAudioMetadataItems interface [Core Audio]","described","coreaudio.ispatialaudiometadataitems","spatialaudiometadata/ISpatialAudioMetadataItems"]
old-location: coreaudio\ispatialaudiometadataitems.htm
tech.root: CoreAudio
ms.assetid: 54A6B7DE-A41E-4214-AF02-CC19250B9037
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataItems, ISpatialAudioMetadataItems interface [Core Audio], ISpatialAudioMetadataItems interface [Core Audio],described, coreaudio.ispatialaudiometadataitems, spatialaudiometadata/ISpatialAudioMetadataItems
req.header: spatialaudiometadata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioMetadataItems
 - spatialaudiometadata/ISpatialAudioMetadataItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataItems
---

# ISpatialAudioMetadataItems interface


## -description

Represents a buffer of spatial audio metadata items. Metadata commands and values can be written to, read from, and copied between ISpatialAudioMetadataItems using the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>, <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>, and <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a> interfaces. Use caller-allocated memory to store metadata items by creating an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a>.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioMetadataItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataItems</b> also has these types of members:

## -remarks

Get an instance of this interface by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems</a>.
