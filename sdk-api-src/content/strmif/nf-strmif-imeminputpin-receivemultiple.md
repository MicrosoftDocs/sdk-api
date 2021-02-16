---
UID: NF:strmif.IMemInputPin.ReceiveMultiple
title: IMemInputPin::ReceiveMultiple (strmif.h)
description: The ReceiveMultiple method receives multiple samples in the stream.
helpviewer_keywords: ["IMemInputPin interface [DirectShow]","ReceiveMultiple method","IMemInputPin.ReceiveMultiple","IMemInputPin::ReceiveMultiple","IMemInputPinReceiveMultiple","ReceiveMultiple","ReceiveMultiple method [DirectShow]","ReceiveMultiple method [DirectShow]","IMemInputPin interface","dshow.imeminputpin_receivemultiple","strmif/IMemInputPin::ReceiveMultiple"]
old-location: dshow\imeminputpin_receivemultiple.htm
tech.root: dshow
ms.assetid: cf90a6e8-0758-4cee-887d-3ac9f7aa764d
ms.date: 12/05/2018
ms.keywords: IMemInputPin interface [DirectShow],ReceiveMultiple method, IMemInputPin.ReceiveMultiple, IMemInputPin::ReceiveMultiple, IMemInputPinReceiveMultiple, ReceiveMultiple, ReceiveMultiple method [DirectShow], ReceiveMultiple method [DirectShow],IMemInputPin interface, dshow.imeminputpin_receivemultiple, strmif/IMemInputPin::ReceiveMultiple
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
 - IMemInputPin::ReceiveMultiple
 - strmif/IMemInputPin::ReceiveMultiple
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
 - IMemInputPin.ReceiveMultiple
---

# IMemInputPin::ReceiveMultiple


## -description

The <code>ReceiveMultiple</code> method receives multiple samples in the stream.

## -parameters

### -param pSamples [in]

Address of an array of <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface pointers, of size <i>nSamples</i>.

### -param nSamples [in]

Number of samples to process.

### -param nSamplesProcessed [out]

Pointer to a variable that receives the number of samples that were processed.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Pin is currently flushing; sample was rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Invalid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_RUNTIME_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A run-time error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is stopped.

</td>
</tr>
</table>

## -remarks

This method behaves like the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> method, but receives an array of samples.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>