---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.GetID
title: IMFSpatialAudioObjectBuffer::GetID (mfspatialaudio.h)
description: Returns the unique, unsigned 32-bit ID of the spatial audio object represented by the buffer.
old-location: mf\imfspatialaudioobjectbuffer_getid.htm
tech.root: medfound
ms.assetid: 5BB0DEB2-B3B9-4723-973D-A9296D94DDE6
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [Media Foundation], GetID method [Media Foundation],IMFSpatialAudioObjectBuffer interface, IMFSpatialAudioObjectBuffer interface [Media Foundation],GetID method, IMFSpatialAudioObjectBuffer.GetID, IMFSpatialAudioObjectBuffer::GetID, mf.imfspatialaudioobjectbuffer_getid, mfspatialaudio/IMFSpatialAudioObjectBuffer::GetID
ms.topic: method
f1_keywords:
- mfspatialaudio/IMFSpatialAudioObjectBuffer.GetID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfobjects.lib
- mfobjects.dll
api_name:
- IMFSpatialAudioObjectBuffer.GetID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSpatialAudioObjectBuffer::GetID


## -description


Returns the unique, unsigned 32-bit ID of the spatial audio object represented by the buffer.
    If <a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-setid">SetID</a> method was not previously called, this method returns the invalid object ID, -1 
    (0xffffffff).  The invalid ID indicates that the object buffer is unused and
    contains invalid data.


## -parameters




### -param pu32ID [out]

Pointer to a 32-bit variable where the object ID will be stored.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a>
 

 

