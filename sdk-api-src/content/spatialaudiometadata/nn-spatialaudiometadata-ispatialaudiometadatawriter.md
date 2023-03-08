---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataWriter
title: ISpatialAudioMetadataWriter (spatialaudiometadata.h)
description: Provides methods for storing spatial audio metadata items positioned within a range of corresponding audio frames.
helpviewer_keywords: ["ISpatialAudioMetadataWriter","ISpatialAudioMetadataWriter interface [Core Audio]","ISpatialAudioMetadataWriter interface [Core Audio]","described","coreaudio.ispatialaudiometadatawriter","spatialaudiometadata/ISpatialAudioMetadataWriter"]
old-location: coreaudio\ispatialaudiometadatawriter.htm
tech.root: CoreAudio
ms.assetid: F8CD8B79-9442-46D0-ABF5-5F6734474B01
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataWriter, ISpatialAudioMetadataWriter interface [Core Audio], ISpatialAudioMetadataWriter interface [Core Audio],described, coreaudio.ispatialaudiometadatawriter, spatialaudiometadata/ISpatialAudioMetadataWriter
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
 - ISpatialAudioMetadataWriter
 - spatialaudiometadata/ISpatialAudioMetadataWriter
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
 - ISpatialAudioMetadataWriter
---

# ISpatialAudioMetadataWriter interface


## -description

Provides methods for storing spatial audio metadata items
positioned within a range of corresponding audio frames.  Each metadata item has a zero-based 
offset position within the specified frame.  Each item can contain one or more commands
specific to the metadata format ID provided in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataclient">ISpatialAudioMetadataClient</a> was created.  
This object does not allocate storage for the metadata it is provided, the caller is expected to manage the allocation of memory used to store the packed data.
Multiple metadata items can be placed in the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.  For each item, 
call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitem">WriteNextItem</a> followed by a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitemcommand">WriteNextItemCommand</a>.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioMetadataWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataWriter</b> also has these types of members:

