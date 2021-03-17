---
UID: NF:mediaobj.IMediaObject.ProcessInput
title: IMediaObject::ProcessInput (mediaobj.h)
description: The ProcessInput method delivers a buffer to the specified input stream.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","ProcessInput method","IMediaObject.ProcessInput","IMediaObject::ProcessInput","IMediaObjectProcessInput","ProcessInput","ProcessInput method [DirectShow]","ProcessInput method [DirectShow]","IMediaObject interface","dshow.imediaobject_processinput","mediaobj/IMediaObject::ProcessInput"]
old-location: dshow\imediaobject_processinput.htm
tech.root: dshow
ms.assetid: f52e9586-f65d-418f-8c1a-c97c0a81d253
ms.date: 12/05/2018
ms.keywords: IMediaObject interface [DirectShow],ProcessInput method, IMediaObject.ProcessInput, IMediaObject::ProcessInput, IMediaObjectProcessInput, ProcessInput, ProcessInput method [DirectShow], ProcessInput method [DirectShow],IMediaObject interface, dshow.imediaobject_processinput, mediaobj/IMediaObject::ProcessInput
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::ProcessInput
 - mediaobj/IMediaObject::ProcessInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.ProcessInput
---

# IMediaObject::ProcessInput


## -description

The <code>ProcessInput</code> method delivers a buffer to the specified input stream.

## -parameters

### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.

### -param pBuffer

Pointer to the buffer's <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer</a> interface.

### -param dwFlags

Bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_input_data_buffer_flags">DMO_INPUT_DATA_BUFFER_FLAGS</a> enumeration.

### -param rtTimestamp

Time stamp that specifies the start time of the data in the buffer. If the buffer has a valid time stamp, set the DMO_INPUT_DATA_BUFFERF_TIME flag in the <i>dwFlags</i> parameter. Otherwise, the DMO ignores this value.

### -param rtTimelength

Reference time specifying the duration of the data in the buffer. If this value is valid, set the DMO_INPUT_DATA_BUFFERF_TIMELENGTH flag in the <i>dwFlags</i> parameter. Otherwise, the DMO ignores this value.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
Data cannot be accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No output to process.

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

The input buffer specified in the <i>pBuffer</i> parameter is read-only. The DMO will not modify the data in this buffer. All write operations occur on the output buffers, which are given in a separate call to the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a> method.

If the DMO does not process all the data in the buffer, it keeps a reference count on the buffer. It releases the buffer once it has generated all the output, unless it needs to perform lookahead on the data. (To determine whether a DMO performs lookahead, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo">IMediaObject::GetInputStreamInfo</a> method.)

If this method returns DMO_E_NOTACCEPTING, call <b>ProcessOutput</b> until the input stream can accept more data. To determine whether the stream can accept more data, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputstatus">IMediaObject::GetInputStatus</a> method.

If the method returns S_FALSE, no output was generated from this input and the application does not need to call <b>ProcessOutput</b>. However, a DMO is not required to return S_FALSE in this situation; it might return S_OK.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>