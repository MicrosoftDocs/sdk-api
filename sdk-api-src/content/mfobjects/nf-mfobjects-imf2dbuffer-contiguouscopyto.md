---
UID: NF:mfobjects.IMF2DBuffer.ContiguousCopyTo
title: IMF2DBuffer::ContiguousCopyTo (mfobjects.h)
description: Copies this buffer into the caller's buffer, converting the data to contiguous format.
helpviewer_keywords: ["32601f2e-ab91-4a65-bcf4-8e063e90fbb0","ContiguousCopyTo","ContiguousCopyTo method [Media Foundation]","ContiguousCopyTo method [Media Foundation]","IMF2DBuffer interface","IMF2DBuffer interface [Media Foundation]","ContiguousCopyTo method","IMF2DBuffer.ContiguousCopyTo","IMF2DBuffer::ContiguousCopyTo","mf.imf2dbuffer_contiguouscopyto","mfobjects/IMF2DBuffer::ContiguousCopyTo"]
old-location: mf\imf2dbuffer_contiguouscopyto.htm
tech.root: mf
ms.assetid: 32601f2e-ab91-4a65-bcf4-8e063e90fbb0
ms.date: 12/05/2018
ms.keywords: 32601f2e-ab91-4a65-bcf4-8e063e90fbb0, ContiguousCopyTo, ContiguousCopyTo method [Media Foundation], ContiguousCopyTo method [Media Foundation],IMF2DBuffer interface, IMF2DBuffer interface [Media Foundation],ContiguousCopyTo method, IMF2DBuffer.ContiguousCopyTo, IMF2DBuffer::ContiguousCopyTo, mf.imf2dbuffer_contiguouscopyto, mfobjects/IMF2DBuffer::ContiguousCopyTo
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
 - IMF2DBuffer::ContiguousCopyTo
 - mfobjects/IMF2DBuffer::ContiguousCopyTo
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
 - IMF2DBuffer.ContiguousCopyTo
---

# IMF2DBuffer::ContiguousCopyTo


## -description

Copies this buffer into the caller's buffer, converting the data to contiguous format.

## -parameters

### -param pbDestBuffer [out]

Pointer to the destination buffer where the data will be copied. The caller allocates the buffer.

### -param cbDestBuffer [in]

Size of the destination buffer, in bytes. To get the required size, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-getcontiguouslength">IMF2DBuffer::GetContiguousLength</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid size specified in <i>pbDestBuffer</i>.

</td>
</tr>
</table>

## -remarks

If the original buffer is not contiguous, this method converts the contents into contiguous format during the copy. For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>