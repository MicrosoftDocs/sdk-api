---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.GetType
title: IMFSpatialAudioObjectBuffer::GetType (mfspatialaudio.h)
description: Gets the type of the spatial audio object represented by the buffer. If SetType has not been called previously, this method returns the default value of AudioObjectType_None.
helpviewer_keywords: ["GetType","GetType method [Media Foundation]","GetType method [Media Foundation]","IMFSpatialAudioObjectBuffer interface","IMFSpatialAudioObjectBuffer interface [Media Foundation]","GetType method","IMFSpatialAudioObjectBuffer.GetType","IMFSpatialAudioObjectBuffer::GetType","mf.imfspatialaudioobjectbuffer_gettype","mfspatialaudio/IMFSpatialAudioObjectBuffer::GetType"]
old-location: mf\imfspatialaudioobjectbuffer_gettype.htm
tech.root: mf
ms.assetid: CF0285D2-E56B-44A5-B7E0-3227213D9523
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Media Foundation], GetType method [Media Foundation],IMFSpatialAudioObjectBuffer interface, IMFSpatialAudioObjectBuffer interface [Media Foundation],GetType method, IMFSpatialAudioObjectBuffer.GetType, IMFSpatialAudioObjectBuffer::GetType, mf.imfspatialaudioobjectbuffer_gettype, mfspatialaudio/IMFSpatialAudioObjectBuffer::GetType
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
 - IMFSpatialAudioObjectBuffer::GetType
 - mfspatialaudio/IMFSpatialAudioObjectBuffer::GetType
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
 - IMFSpatialAudioObjectBuffer.GetType
---

# IMFSpatialAudioObjectBuffer::GetType


## -description

Gets the type of the spatial audio object represented by the buffer. If <a href="/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-settype">SetType</a> has not been called previously, this method returns the default value of <b>AudioObjectType_None</b>.

## -parameters

### -param pType [out]

A pointer to an <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> variable where the audio object type will be stored.

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

## -see-also

<a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a>