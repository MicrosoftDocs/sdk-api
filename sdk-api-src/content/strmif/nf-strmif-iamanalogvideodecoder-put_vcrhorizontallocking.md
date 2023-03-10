---
UID: NF:strmif.IAMAnalogVideoDecoder.put_VCRHorizontalLocking
title: IAMAnalogVideoDecoder::put_VCRHorizontalLocking (strmif.h)
description: The put_VCRHorizontalLocking method specifies whether the video is a tape source or a broadcast source.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","put_VCRHorizontalLocking method","IAMAnalogVideoDecoder.put_VCRHorizontalLocking","IAMAnalogVideoDecoder::put_VCRHorizontalLocking","IAMAnalogVideoDecoderput_VCRHorizontalLocking","dshow.iamanalogvideodecoder_put_vcrhorizontallocking","put_VCRHorizontalLocking","put_VCRHorizontalLocking method [DirectShow]","put_VCRHorizontalLocking method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking"]
old-location: dshow\iamanalogvideodecoder_put_vcrhorizontallocking.htm
tech.root: dshow
ms.assetid: 4b215f8b-dfd9-40cf-a392-7cc42b17b214
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],put_VCRHorizontalLocking method, IAMAnalogVideoDecoder.put_VCRHorizontalLocking, IAMAnalogVideoDecoder::put_VCRHorizontalLocking, IAMAnalogVideoDecoderput_VCRHorizontalLocking, dshow.iamanalogvideodecoder_put_vcrhorizontallocking, put_VCRHorizontalLocking, put_VCRHorizontalLocking method [DirectShow], put_VCRHorizontalLocking method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAnalogVideoDecoder::put_VCRHorizontalLocking
 - strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAnalogVideoDecoder.put_VCRHorizontalLocking
---

# IAMAnalogVideoDecoder::put_VCRHorizontalLocking


## -description

The <code>put_VCRHorizontalLocking</code> method specifies whether the video is a tape source or a broadcast source.

## -parameters

### -param lVCRHorizontalLocking [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The video is from a broadcast source.</td>
</tr>
<tr>
<td>1</td>
<td>The video is from a tape source.</td>
</tr>
</table>

## -returns

Returns an HRESULT value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The timing accuracy of synchronization pulses is typically poorer from a tape source than from a broadcast source. Setting the value to 1 tells the decoder to relax its standards, which leads to a better chance of maintaining sync.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>