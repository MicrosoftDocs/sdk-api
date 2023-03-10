---
UID: NF:wmcodecdsp.IWMCodecLeakyBucket.SetBufferSizeBits
title: IWMCodecLeakyBucket::SetBufferSizeBits (wmcodecdsp.h)
description: Sets the buffer size in bits.
helpviewer_keywords: ["IWMCodecLeakyBucket interface [Media Foundation]","SetBufferSizeBits method","IWMCodecLeakyBucket.SetBufferSizeBits","IWMCodecLeakyBucket::SetBufferSizeBits","SetBufferSizeBits","SetBufferSizeBits method [Media Foundation]","SetBufferSizeBits method [Media Foundation]","IWMCodecLeakyBucket interface","codecapi.iwmcodecleakybucketsetbuffersizebits","mf.iwmcodecleakybucketsetbuffersizebits","wmcodecdsp/IWMCodecLeakyBucket::SetBufferSizeBits"]
old-location: mf\iwmcodecleakybucketsetbuffersizebits.htm
tech.root: mf
ms.assetid: b602e8ca-8446-4f94-bcd0-193084d96565
ms.date: 12/05/2018
ms.keywords: IWMCodecLeakyBucket interface [Media Foundation],SetBufferSizeBits method, IWMCodecLeakyBucket.SetBufferSizeBits, IWMCodecLeakyBucket::SetBufferSizeBits, SetBufferSizeBits, SetBufferSizeBits method [Media Foundation], SetBufferSizeBits method [Media Foundation],IWMCodecLeakyBucket interface, codecapi.iwmcodecleakybucketsetbuffersizebits, mf.iwmcodecleakybucketsetbuffersizebits, wmcodecdsp/IWMCodecLeakyBucket::SetBufferSizeBits
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMCodecLeakyBucket::SetBufferSizeBits
 - wmcodecdsp/IWMCodecLeakyBucket::SetBufferSizeBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecLeakyBucket.SetBufferSizeBits
---

# IWMCodecLeakyBucket::SetBufferSizeBits


## -description

Sets the buffer size in bits.

## -parameters

### -param ulBufferSize [in]

The buffer size, in bits.

## -returns

This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

This method is not implemented on the audio encoder objects. If you call this method from the <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket">IWMCodecLeakyBucket</a> interface it returns E_NOTIMPL.

The buffer size is equal to the bit rate of the stream multiplied by the buffer window. For example, a stream with a bit rate of 28 kilobits per second with a buffer window of 3 seconds would have a buffer of 28000 bits per second x 3 seconds = 84000 bits.

This method is an alternative to setting the MFPKEY_VIDEOWINDOW property. Using this method does not alter the bit rate of the stream, but does alter the buffer window. Using the stream with a bit rate of 28000 bits per second from the previous example, setting the buffer size to 84000 using this method would have exactly the same effect as setting <a href="/windows/desktop/medfound/mfpkey-videowindowproperty">MFPKEY_VIDEOWINDOW</a> to 3000 milliseconds (3 seconds).

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket">IWMCodecLeakyBucket Interface</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecleakybucket-getbuffersizebits">IWMCodecLeakyBucket::GetBufferSizeBits</a>