---
UID: NF:wmsbuffer.INSSBuffer.GetBuffer
title: INSSBuffer::GetBuffer (wmsbuffer.h)
description: The GetBuffer method retrieves the location of the buffer controlled by the buffer object.
helpviewer_keywords: ["GetBuffer","GetBuffer method [windows Media Format]","GetBuffer method [windows Media Format]","INSSBuffer interface","INSSBuffer interface [windows Media Format]","GetBuffer method","INSSBuffer.GetBuffer","INSSBuffer::GetBuffer","INSSBufferGetBuffer","wmformat.inssbuffer_getbuffer","wmsbuffer/INSSBuffer::GetBuffer"]
old-location: wmformat\inssbuffer_getbuffer.htm
tech.root: wmformat
ms.assetid: 3f9e8408-52ce-48aa-ba85-51bdbbfd8b51
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [windows Media Format], GetBuffer method [windows Media Format],INSSBuffer interface, INSSBuffer interface [windows Media Format],GetBuffer method, INSSBuffer.GetBuffer, INSSBuffer::GetBuffer, INSSBufferGetBuffer, wmformat.inssbuffer_getbuffer, wmsbuffer/INSSBuffer::GetBuffer
req.header: wmsbuffer.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSSBuffer::GetBuffer
 - wmsbuffer/INSSBuffer::GetBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSSBuffer.GetBuffer
---

# INSSBuffer::GetBuffer


## -description

The <b>GetBuffer</b> method retrieves the location of the buffer controlled by the buffer object. Buffers are used to store samples. When passing samples to the writer, you need the location of the buffer so you can copy your samples into it. When you copy data to the address returned by this call, you must call <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-setlength">INSSBuffer::SetLength</a> to specify how much of the buffer actually contains data.



When receiving samples from the reader or synchronous reader, retrieve the size of the buffer at the same time as the location by calling <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength">INSSBuffer::GetBufferAndLength</a>.

## -parameters

### -param ppdwBuffer [out]

Pointer to a pointer to the buffer.

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
The <i>ppdwBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength">INSSBuffer::GetBufferAndLength</a>