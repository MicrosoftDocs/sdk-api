---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataCopier
title: ISpatialAudioMetadataCopier (spatialaudiometadata.h)
description: Provides methods for copying all or subsets of metadata items from a source SpatialAudioMetadataItems into a destination SpatialAudioMetadataItems.
helpviewer_keywords: ["ISpatialAudioMetadataCopier","ISpatialAudioMetadataCopier interface [Core Audio]","ISpatialAudioMetadataCopier interface [Core Audio]","described","coreaudio.ispatialaudiometadatacopier","spatialaudiometadata/ISpatialAudioMetadataCopier"]
old-location: coreaudio\ispatialaudiometadatacopier.htm
tech.root: CoreAudio
ms.assetid: 74708744-78BF-4135-BB0A-50A7CA41ECDD
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataCopier, ISpatialAudioMetadataCopier interface [Core Audio], ISpatialAudioMetadataCopier interface [Core Audio],described, coreaudio.ispatialaudiometadatacopier, spatialaudiometadata/ISpatialAudioMetadataCopier
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
 - ISpatialAudioMetadataCopier
 - spatialaudiometadata/ISpatialAudioMetadataCopier
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
 - ISpatialAudioMetadataCopier
---

# ISpatialAudioMetadataCopier interface


## -description

Provides methods for copying all or subsets of metadata items from a source <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">SpatialAudioMetadataItems</a> into a destination <b>SpatialAudioMetadataItems</b>.
The <b>SpatialAudioMetadataItems</b> object, which is populated using an  <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> or <b>ISpatialAudioMetadataCopier</b>, has a frame count, specified with the <i>frameCount</i> parameter to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>,
that represents the valid range of metadata item offsets.  <b>ISpatialAudioMetadataReader</b> enables copying
groups of items within a subrange of the total frame count.  The object
maintains an internal read position, which is advanced by the number of frames specified when a copy operation is performed.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioMetadataCopier</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataCopier</b> also has these types of members:

