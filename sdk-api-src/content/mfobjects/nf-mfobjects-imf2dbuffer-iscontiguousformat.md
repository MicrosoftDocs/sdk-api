---
UID: NF:mfobjects.IMF2DBuffer.IsContiguousFormat
title: IMF2DBuffer::IsContiguousFormat (mfobjects.h)
description: Queries whether the buffer is contiguous in its native format.
helpviewer_keywords: ["IMF2DBuffer interface [Media Foundation]","IsContiguousFormat method","IMF2DBuffer.IsContiguousFormat","IMF2DBuffer::IsContiguousFormat","IsContiguousFormat","IsContiguousFormat method [Media Foundation]","IsContiguousFormat method [Media Foundation]","IMF2DBuffer interface","a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e","mf.imf2dbuffer_iscontiguousformat","mfobjects/IMF2DBuffer::IsContiguousFormat"]
old-location: mf\imf2dbuffer_iscontiguousformat.htm
tech.root: mf
ms.assetid: a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e
ms.date: 12/05/2018
ms.keywords: IMF2DBuffer interface [Media Foundation],IsContiguousFormat method, IMF2DBuffer.IsContiguousFormat, IMF2DBuffer::IsContiguousFormat, IsContiguousFormat, IsContiguousFormat method [Media Foundation], IsContiguousFormat method [Media Foundation],IMF2DBuffer interface, a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e, mf.imf2dbuffer_iscontiguousformat, mfobjects/IMF2DBuffer::IsContiguousFormat
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
 - IMF2DBuffer::IsContiguousFormat
 - mfobjects/IMF2DBuffer::IsContiguousFormat
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
 - IMF2DBuffer.IsContiguousFormat
---

# IMF2DBuffer::IsContiguousFormat


## -description

Queries whether the buffer is contiguous in its native format.

## -parameters

### -param pfIsContiguous [out]

Receives a Boolean value. The value is <b>TRUE</b> if the buffer is contiguous, and <b>FALSE</b> otherwise.

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

For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface. For non-contiguous buffers, the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a> method must perform an internal copy.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>