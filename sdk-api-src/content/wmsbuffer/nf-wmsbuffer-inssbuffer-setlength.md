---
UID: NF:wmsbuffer.INSSBuffer.SetLength
title: INSSBuffer::SetLength (wmsbuffer.h)
description: The SetLength method specifies the size of the used portion of the buffer.
helpviewer_keywords: ["INSSBuffer interface [windows Media Format]","SetLength method","INSSBuffer.SetLength","INSSBuffer::SetLength","INSSBufferSetLength","SetLength","SetLength method [windows Media Format]","SetLength method [windows Media Format]","INSSBuffer interface","wmformat.inssbuffer_setlength","wmsbuffer/INSSBuffer::SetLength"]
old-location: wmformat\inssbuffer_setlength.htm
tech.root: wmformat
ms.assetid: 3f0e8d8a-efc7-4f1b-8a42-7907439ed8af
ms.date: 4/26/2023
ms.keywords: INSSBuffer interface [windows Media Format],SetLength method, INSSBuffer.SetLength, INSSBuffer::SetLength, INSSBufferSetLength, SetLength, SetLength method [windows Media Format], SetLength method [windows Media Format],INSSBuffer interface, wmformat.inssbuffer_setlength, wmsbuffer/INSSBuffer::SetLength
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
 - INSSBuffer::SetLength
 - wmsbuffer/INSSBuffer::SetLength
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
 - INSSBuffer.SetLength
---

# INSSBuffer::SetLength


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetLength</b> method specifies the size of the used portion of the buffer. If you are storing a sample in the buffer, call <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer">INSSBuffer::GetBuffer</a> to retrieve the address of the buffer. Then copy your data to that address and use this method to set the length of the used portion of the buffer.

## -parameters

### -param dwLength [in]

<b>DWORD</b> containing the size of the used portion, in bytes.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwLength</i> is greater than the buffer size.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getlength">INSSBuffer::GetLength</a>