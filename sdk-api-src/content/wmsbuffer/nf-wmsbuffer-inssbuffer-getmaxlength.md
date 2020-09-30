---
UID: NF:wmsbuffer.INSSBuffer.GetMaxLength
title: INSSBuffer::GetMaxLength (wmsbuffer.h)
description: The GetMaxLength method retrieves the maximum size to which a buffer can be set.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [windows Media Format]","GetMaxLength method [windows Media Format]","INSSBuffer interface","INSSBuffer interface [windows Media Format]","GetMaxLength method","INSSBuffer.GetMaxLength","INSSBuffer::GetMaxLength","INSSBufferGetMaxLength","wmformat.inssbuffer_getmaxlength","wmsbuffer/INSSBuffer::GetMaxLength"]
old-location: wmformat\inssbuffer_getmaxlength.htm
tech.root: wmformat
ms.assetid: 6b386c24-1737-4e30-98fa-444fc8a34503
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [windows Media Format], GetMaxLength method [windows Media Format],INSSBuffer interface, INSSBuffer interface [windows Media Format],GetMaxLength method, INSSBuffer.GetMaxLength, INSSBuffer::GetMaxLength, INSSBufferGetMaxLength, wmformat.inssbuffer_getmaxlength, wmsbuffer/INSSBuffer::GetMaxLength
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
 - INSSBuffer::GetMaxLength
 - wmsbuffer/INSSBuffer::GetMaxLength
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
 - INSSBuffer.GetMaxLength
---

# INSSBuffer::GetMaxLength


## -description

The <b>GetMaxLength</b> method retrieves the maximum size to which a buffer can be set. The maximum value is set when the sample is created. If you are using <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample">IWMWriter::AllocateSample</a>, the size you specify becomes the maximum buffer length. The actual amount of the buffer that is used can be retrieved by calling <a href="/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getlength">INSSBuffer::GetLength</a>.

## -parameters

### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the maximum length, in bytes.

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
The <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The maximum size of the buffer as returned by this method does not affect or reflect the size of any data unit extensions associated with the sample stored in the buffer.

## -see-also

<a href="/windows/desktop/wmformat/data-unit-extensions">Data Unit Extensions</a>



<a href="/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getlength">INSSBuffer::GetLength</a>