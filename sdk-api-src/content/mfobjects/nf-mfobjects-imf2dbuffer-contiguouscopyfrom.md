---
UID: NF:mfobjects.IMF2DBuffer.ContiguousCopyFrom
title: IMF2DBuffer::ContiguousCopyFrom (mfobjects.h)
description: Copies data to this buffer from a buffer that has a contiguous format.
helpviewer_keywords: ["84634782-7805-4e2b-a043-7e49adef5c2a","ContiguousCopyFrom","ContiguousCopyFrom method [Media Foundation]","ContiguousCopyFrom method [Media Foundation]","IMF2DBuffer interface","IMF2DBuffer interface [Media Foundation]","ContiguousCopyFrom method","IMF2DBuffer.ContiguousCopyFrom","IMF2DBuffer::ContiguousCopyFrom","mf.imf2dbuffer_contiguouscopyfrom","mfobjects/IMF2DBuffer::ContiguousCopyFrom"]
old-location: mf\imf2dbuffer_contiguouscopyfrom.htm
tech.root: mf
ms.assetid: 84634782-7805-4e2b-a043-7e49adef5c2a
ms.date: 12/05/2018
ms.keywords: 84634782-7805-4e2b-a043-7e49adef5c2a, ContiguousCopyFrom, ContiguousCopyFrom method [Media Foundation], ContiguousCopyFrom method [Media Foundation],IMF2DBuffer interface, IMF2DBuffer interface [Media Foundation],ContiguousCopyFrom method, IMF2DBuffer.ContiguousCopyFrom, IMF2DBuffer::ContiguousCopyFrom, mf.imf2dbuffer_contiguouscopyfrom, mfobjects/IMF2DBuffer::ContiguousCopyFrom
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
 - IMF2DBuffer::ContiguousCopyFrom
 - mfobjects/IMF2DBuffer::ContiguousCopyFrom
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
 - IMF2DBuffer.ContiguousCopyFrom
---

# IMF2DBuffer::ContiguousCopyFrom


## -description

Copies data to this buffer from a buffer that has a contiguous format.

## -parameters

### -param pbSrcBuffer [in]

Pointer to the source buffer. The caller allocates the buffer.

### -param cbSrcBuffer [in]

Size of the source buffer, in bytes. To get the maximum size of the buffer, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-getcontiguouslength">IMF2DBuffer::GetContiguousLength</a>.

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

This method copies the contents of the source buffer into the buffer that is managed by this <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> object. The source buffer must be in contiguous format. While copying, the method converts the contents into the destination buffer's native format, correcting for the buffer's pitch if necessary.

For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface topic.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>