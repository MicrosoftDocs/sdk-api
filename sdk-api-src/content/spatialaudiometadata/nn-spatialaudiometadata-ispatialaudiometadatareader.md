---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataReader
title: ISpatialAudioMetadataReader (spatialaudiometadata.h)
description: Provides methods for extracting spatial audio metadata items and item command value pairs from an ISpatialAudioMetadataItems object.
helpviewer_keywords: ["ISpatialAudioMetadataReader","ISpatialAudioMetadataReader interface [Core Audio]","ISpatialAudioMetadataReader interface [Core Audio]","described","coreaudio.ispatialaudiometadatareader","spatialaudiometadata/ISpatialAudioMetadataReader"]
old-location: coreaudio\ispatialaudiometadatareader.htm
tech.root: CoreAudio
ms.assetid: BD1AD4CE-6E88-4292-AA79-E71FE00C2078
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataReader, ISpatialAudioMetadataReader interface [Core Audio], ISpatialAudioMetadataReader interface [Core Audio],described, coreaudio.ispatialaudiometadatareader, spatialaudiometadata/ISpatialAudioMetadataReader
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
 - ISpatialAudioMetadataReader
 - spatialaudiometadata/ISpatialAudioMetadataReader
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
 - ISpatialAudioMetadataReader
---

# ISpatialAudioMetadataReader interface


## -description

Provides methods for extracting
spatial audio metadata items and item command value pairs from an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.
The <b>SpatialAudioMetadataItems</b> object, which is populated using an  <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> or <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a>, has a frame count, specified with the <i>frameCount</i> parameter to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>,
that represents the valid range of metadata item offsets.  <b>ISpatialAudioMetadataReader</b> enables reading back
groups of items within a subrange of the total frame count.  The object
maintains an internal read position, which is advanced by the number of frames specified when read operation is performed.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioMetadataReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataReader</b> also has these types of members:

