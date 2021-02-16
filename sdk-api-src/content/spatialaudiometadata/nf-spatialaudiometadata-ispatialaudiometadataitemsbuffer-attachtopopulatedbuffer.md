---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataItemsBuffer.AttachToPopulatedBuffer
title: ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer (spatialaudiometadata.h)
description: Attaches a previously populated buffer for storage of ISpatialAudioMetadataItems objects. The metadata items already in the buffer are retained.
helpviewer_keywords: ["AttachToPopulatedBuffer","AttachToPopulatedBuffer method [Core Audio]","AttachToPopulatedBuffer method [Core Audio]","ISpatialAudioMetadataItemsBuffer interface","ISpatialAudioMetadataItemsBuffer interface [Core Audio]","AttachToPopulatedBuffer method","ISpatialAudioMetadataItemsBuffer.AttachToPopulatedBuffer","ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer","coreaudio.ispatialaudiometadataitemsbuffer_attachtopopulatedbuffer","spatialaudiometadata/ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer"]
old-location: coreaudio\ispatialaudiometadataitemsbuffer_attachtopopulatedbuffer.htm
tech.root: CoreAudio
ms.assetid: 7C17F504-6EB7-4A8D-B3E1-203D5D9B7E3C
ms.date: 12/05/2018
ms.keywords: AttachToPopulatedBuffer, AttachToPopulatedBuffer method [Core Audio], AttachToPopulatedBuffer method [Core Audio],ISpatialAudioMetadataItemsBuffer interface, ISpatialAudioMetadataItemsBuffer interface [Core Audio],AttachToPopulatedBuffer method, ISpatialAudioMetadataItemsBuffer.AttachToPopulatedBuffer, ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer, coreaudio.ispatialaudiometadataitemsbuffer_attachtopopulatedbuffer, spatialaudiometadata/ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer
 - spatialaudiometadata/ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer
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
 - ISpatialAudioMetadataItemsBuffer.AttachToPopulatedBuffer
---

# ISpatialAudioMetadataItemsBuffer::AttachToPopulatedBuffer


## -description

Attaches a previously populated buffer for storage of <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> objects. The metadata items already in the buffer are retained.

## -parameters

### -param buffer [in]

A pointer to memory to use for storage.

### -param bufferLength

The length of the supplied buffer. This size must match the length required for the metadata format and maximum metadata item count.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened for copying with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-open">Open</a> or the object has been closed for writing with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-close">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_BUFFER_ALREADY_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer has already been attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_ATTACH_FAILED_INTERNAL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> was created to use a media pipeline internal buffer, so an external buffer can't be attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The supplied populated buffer uses a format that is different from the current format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

The supplied buffer is not large enough to hold the maximum number of metadata items. Call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-getspatialaudiometadataitemsbufferlength">GetSpatialAudioMetadataItemsBufferLength</a> to determine the required buffer size.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a>