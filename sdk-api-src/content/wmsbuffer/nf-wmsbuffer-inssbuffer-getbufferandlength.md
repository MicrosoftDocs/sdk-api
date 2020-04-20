---
UID: NF:wmsbuffer.INSSBuffer.GetBufferAndLength
title: INSSBuffer::GetBufferAndLength (wmsbuffer.h)
description: The GetBufferAndLength method retrieves the location and size of the used portion of the buffer controlled by the buffer object.helpviewer_keywords: ["GetBufferAndLength","GetBufferAndLength method [windows Media Format]","GetBufferAndLength method [windows Media Format]","INSSBuffer interface","INSSBuffer interface [windows Media Format]","GetBufferAndLength method","INSSBuffer.GetBufferAndLength","INSSBuffer::GetBufferAndLength","INSSBufferGetBufferAndLength","wmformat.inssbuffer_getbufferandlength","wmsbuffer/INSSBuffer::GetBufferAndLength"]
old-location: wmformat\inssbuffer_getbufferandlength.htm
tech.root: wmformat
ms.assetid: cb03d006-fbaa-4971-8022-41a7fa29fb87
ms.date: 12/05/2018
ms.keywords: GetBufferAndLength, GetBufferAndLength method [windows Media Format], GetBufferAndLength method [windows Media Format],INSSBuffer interface, INSSBuffer interface [windows Media Format],GetBufferAndLength method, INSSBuffer.GetBufferAndLength, INSSBuffer::GetBufferAndLength, INSSBufferGetBufferAndLength, wmformat.inssbuffer_getbufferandlength, wmsbuffer/INSSBuffer::GetBufferAndLength
f1_keywords:
- wmsbuffer/INSSBuffer.GetBufferAndLength
dev_langs:
- c++
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
- INSSBuffer.GetBufferAndLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INSSBuffer::GetBufferAndLength


## -description



The <b>GetBufferAndLength</b> method retrieves the location and size of the used portion of the buffer controlled by the buffer object. Buffers are used to store samples. When reading ASF files, you can use the location and length to copy a sample from a buffer delivered by the reader or synchronous reader.




## -parameters




### -param ppdwBuffer [out]

Pointer to a pointer to the buffer.


### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the length of the buffer, in bytes.


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
The <i>ppdwBuffer</i> or <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer">INSSBuffer::GetBuffer</a>
 

 

