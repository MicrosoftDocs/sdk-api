---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataItemsBuffer
title: ISpatialAudioMetadataItemsBuffer (spatialaudiometadata.h)
description: Provides methods for attaching buffers to SpatialAudioMetadataItems for in-place storage of data.
helpviewer_keywords: ["ISpatialAudioMetadataItemsBuffer","ISpatialAudioMetadataItemsBuffer interface [Core Audio]","ISpatialAudioMetadataItemsBuffer interface [Core Audio]","described","coreaudio.ispatialaudiometadataitemsbuffer","spatialaudiometadata/ISpatialAudioMetadataItemsBuffer"]
old-location: coreaudio\ispatialaudiometadataitemsbuffer.htm
tech.root: CoreAudio
ms.assetid: 5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataItemsBuffer, ISpatialAudioMetadataItemsBuffer interface [Core Audio], ISpatialAudioMetadataItemsBuffer interface [Core Audio],described, coreaudio.ispatialaudiometadataitemsbuffer, spatialaudiometadata/ISpatialAudioMetadataItemsBuffer
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
 - ISpatialAudioMetadataItemsBuffer
 - spatialaudiometadata/ISpatialAudioMetadataItemsBuffer
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
 - ISpatialAudioMetadataItemsBuffer
---

# ISpatialAudioMetadataItemsBuffer interface


## -description

Provides methods for attaching buffers to <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">SpatialAudioMetadataItems</a> for in-place storage of data. Get an instance of this object by passing a pointer to the interface into <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>. The buffer will be associated with the returned <b>SpatialAudioMetadataItems</b>. This interface allows you to attach a  buffer and reset its contents to the empty set of metadata items  or attach a  previously-populated     buffer and retain the data stored in the buffer.


This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataItemsBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataItemsBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataItemsBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitemsbuffer-attachtobuffer">AttachToBuffer</a>
</td>
<td align="left" width="63%">
Attaches caller-provided memory for storage of <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitemsbuffer-attachtopopulatedbuffer">AttachToPopulatedBuffer</a>
</td>
<td align="left" width="63%">
Attaches a previously populated buffer for storage of <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> objects. The metadata items already in the buffer are retained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitemsbuffer-detachbuffer">DetachBuffer</a>
</td>
<td align="left" width="63%">
Detaches the buffer.  Memory can only be attached to a single metadata item at a time.

</td>
</tr>
</table>