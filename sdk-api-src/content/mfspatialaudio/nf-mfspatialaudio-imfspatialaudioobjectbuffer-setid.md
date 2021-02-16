---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.SetID
title: IMFSpatialAudioObjectBuffer::SetID (mfspatialaudio.h)
description: Sets the ID of the spatial audio object represented by the buffer.
helpviewer_keywords: ["IMFSpatialAudioObjectBuffer interface [Media Foundation]","SetID method","IMFSpatialAudioObjectBuffer.SetID","IMFSpatialAudioObjectBuffer::SetID","SetID","SetID method [Media Foundation]","SetID method [Media Foundation]","IMFSpatialAudioObjectBuffer interface","mf.imfspatialaudioobjectbuffer_setid","mfspatialaudio/IMFSpatialAudioObjectBuffer::SetID"]
old-location: mf\imfspatialaudioobjectbuffer_setid.htm
tech.root: mf
ms.assetid: 01979492-2CA1-4DAA-8B03-720B521C2D9A
ms.date: 12/05/2018
ms.keywords: IMFSpatialAudioObjectBuffer interface [Media Foundation],SetID method, IMFSpatialAudioObjectBuffer.SetID, IMFSpatialAudioObjectBuffer::SetID, SetID, SetID method [Media Foundation], SetID method [Media Foundation],IMFSpatialAudioObjectBuffer interface, mf.imfspatialaudioobjectbuffer_setid, mfspatialaudio/IMFSpatialAudioObjectBuffer::SetID
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
 - IMFSpatialAudioObjectBuffer::SetID
 - mfspatialaudio/IMFSpatialAudioObjectBuffer::SetID
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
 - IMFSpatialAudioObjectBuffer.SetID
---

# IMFSpatialAudioObjectBuffer::SetID


## -description

Sets the ID of the spatial audio object represented by the buffer.

## -parameters

### -param u32ID

A 32-bit unsigned unique ID of the audio object.

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
</table>

## -remarks

The object ID must be unique for each spatial audio sample.  Subsequent samples can 
    contain spatial audio objects with the same IDs to represent moving dynamic objects or constant
    static objects.

## -see-also

<a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a>