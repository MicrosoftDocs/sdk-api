---
UID: NF:strmif.IAMAnalogVideoEncoder.put_CCEnable
title: IAMAnalogVideoEncoder::put_CCEnable (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_CCEnable method enables or disables closed captioning.
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","put_CCEnable method","IAMAnalogVideoEncoder.put_CCEnable","IAMAnalogVideoEncoder::put_CCEnable","IAMAnalogVideoEncoderput_CCEnable","dshow.iamanalogvideoencoder_put_ccenable","put_CCEnable","put_CCEnable method [DirectShow]","put_CCEnable method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::put_CCEnable"]
old-location: dshow\iamanalogvideoencoder_put_ccenable.htm
tech.root: dshow
ms.assetid: 6513cde7-2765-4225-814b-a619d6a6ab15
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_CCEnable method, IAMAnalogVideoEncoder.put_CCEnable, IAMAnalogVideoEncoder::put_CCEnable, IAMAnalogVideoEncoderput_CCEnable, dshow.iamanalogvideoencoder_put_ccenable, put_CCEnable, put_CCEnable method [DirectShow], put_CCEnable method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_CCEnable
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAMAnalogVideoEncoder::put_CCEnable
 - strmif/IAMAnalogVideoEncoder::put_CCEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.put_CCEnable
---

# IAMAnalogVideoEncoder::put_CCEnable


## -description

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_CCEnable</code> method enables or disables closed captioning.

## -parameters

### -param lCCEnable [in]

Specifies whether closed captioning is on or off as a <b>long</b> integer.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>1</td>
<td>Closed captioning is on.</td>
</tr>
<tr>
<td>0</td>
<td>Closed captioning is off.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>