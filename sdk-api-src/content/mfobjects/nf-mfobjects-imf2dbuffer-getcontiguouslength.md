---
UID: NF:mfobjects.IMF2DBuffer.GetContiguousLength
title: IMF2DBuffer::GetContiguousLength (mfobjects.h)
description: Retrieves the number of bytes needed to store the contents of the buffer in contiguous format.
helpviewer_keywords: ["413d50f6-a047-4561-985d-9d1927825617","GetContiguousLength","GetContiguousLength method [Media Foundation]","GetContiguousLength method [Media Foundation]","IMF2DBuffer interface","IMF2DBuffer interface [Media Foundation]","GetContiguousLength method","IMF2DBuffer.GetContiguousLength","IMF2DBuffer::GetContiguousLength","mf.imf2dbuffer_getcontiguouslength","mfobjects/IMF2DBuffer::GetContiguousLength"]
old-location: mf\imf2dbuffer_getcontiguouslength.htm
tech.root: mf
ms.assetid: 413d50f6-a047-4561-985d-9d1927825617
ms.date: 12/05/2018
ms.keywords: 413d50f6-a047-4561-985d-9d1927825617, GetContiguousLength, GetContiguousLength method [Media Foundation], GetContiguousLength method [Media Foundation],IMF2DBuffer interface, IMF2DBuffer interface [Media Foundation],GetContiguousLength method, IMF2DBuffer.GetContiguousLength, IMF2DBuffer::GetContiguousLength, mf.imf2dbuffer_getcontiguouslength, mfobjects/IMF2DBuffer::GetContiguousLength
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMF2DBuffer::GetContiguousLength
 - mfobjects/IMF2DBuffer::GetContiguousLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMF2DBuffer.GetContiguousLength
---

# IMF2DBuffer::GetContiguousLength


## -description

Retrieves the number of bytes needed to store the contents of the buffer in contiguous format.

## -parameters

### -param pcbLength [out]

Receives the number of bytes needed to store the contents of the buffer in contiguous format.

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

For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>