---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.GetMetadataItems
title: IMFSpatialAudioObjectBuffer::GetMetadataItems (mfspatialaudio.h)
description: Retrieves a pointer to a buffer that may contain spatial audio metadata.
helpviewer_keywords: ["GetMetadataItems","GetMetadataItems method [Media Foundation]","GetMetadataItems method [Media Foundation]","IMFSpatialAudioObjectBuffer interface","IMFSpatialAudioObjectBuffer interface [Media Foundation]","GetMetadataItems method","IMFSpatialAudioObjectBuffer.GetMetadataItems","IMFSpatialAudioObjectBuffer::GetMetadataItems","mf.imfspatialaudioobjectbuffer_getmetadataitems","mfspatialaudio/IMFSpatialAudioObjectBuffer::GetMetadataItems"]
old-location: mf\imfspatialaudioobjectbuffer_getmetadataitems.htm
tech.root: mf
ms.assetid: 19BF7AC6-B21F-47D1-8573-48C5E4869574
ms.date: 12/05/2018
ms.keywords: GetMetadataItems, GetMetadataItems method [Media Foundation], GetMetadataItems method [Media Foundation],IMFSpatialAudioObjectBuffer interface, IMFSpatialAudioObjectBuffer interface [Media Foundation],GetMetadataItems method, IMFSpatialAudioObjectBuffer.GetMetadataItems, IMFSpatialAudioObjectBuffer::GetMetadataItems, mf.imfspatialaudioobjectbuffer_getmetadataitems, mfspatialaudio/IMFSpatialAudioObjectBuffer::GetMetadataItems
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSpatialAudioObjectBuffer::GetMetadataItems
 - mfspatialaudio/IMFSpatialAudioObjectBuffer::GetMetadataItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer.GetMetadataItems
---

# IMFSpatialAudioObjectBuffer::GetMetadataItems


## -description

Retrieves a pointer to a buffer that may 
    contain spatial audio metadata.

## -parameters

### -param ppMetadataItems [out]

A pointer to an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object in which the collection
    of metadata items will be stored.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>

## -remarks

The metadata is written to the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> collection in a format identified by the <a href="/windows/desktop/medfound/mf-mt-spatial-audio-object-metadata-format-id">MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID</a>     media type attribute specified during media type negotiation phase of Media Foundation     topology construction.

## -see-also

<a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a>