---
UID: NF:wmsbuffer.INSSBuffer.GetLength
title: INSSBuffer::GetLength (wmsbuffer.h)
description: The GetLength method retrieves the size of the used portion of the buffer controlled by the buffer object.
helpviewer_keywords: ["GetLength","GetLength method [windows Media Format]","GetLength method [windows Media Format]","INSSBuffer interface","INSSBuffer interface [windows Media Format]","GetLength method","INSSBuffer.GetLength","INSSBuffer::GetLength","INSSBufferGetLength","wmformat.inssbuffer_getlength","wmsbuffer/INSSBuffer::GetLength"]
old-location: wmformat\inssbuffer_getlength.htm
tech.root: wmformat
ms.assetid: a964124d-f25b-442c-a29d-0ee595bdbcce
ms.date: 4/26/2023
ms.keywords: GetLength, GetLength method [windows Media Format], GetLength method [windows Media Format],INSSBuffer interface, INSSBuffer interface [windows Media Format],GetLength method, INSSBuffer.GetLength, INSSBuffer::GetLength, INSSBufferGetLength, wmformat.inssbuffer_getlength, wmsbuffer/INSSBuffer::GetLength
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
 - INSSBuffer::GetLength
 - wmsbuffer/INSSBuffer::GetLength
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
 - INSSBuffer.GetLength
---

# INSSBuffer::GetLength


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLength</b> method retrieves the size of the used portion of the buffer controlled by the buffer object.

## -parameters

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
The <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The allocated buffer may be larger than the used portion. To find the total size of the allocated buffer, call <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getmaxlength">INSSBuffer::GetMaxLength</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-getmaxlength">INSSBuffer::GetMaxLength</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-setlength">INSSBuffer::SetLength</a>