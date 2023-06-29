---
UID: NF:wmsdkidl.IWMWriterFileSink2.GetFileDuration
title: IWMWriterFileSink2::GetFileDuration (wmsdkidl.h)
description: The GetFileDuration method retrieves the duration of the portion of the file that has been written.
helpviewer_keywords: ["GetFileDuration","GetFileDuration method [windows Media Format]","GetFileDuration method [windows Media Format]","IWMWriterFileSink2 interface","IWMWriterFileSink2 interface [windows Media Format]","GetFileDuration method","IWMWriterFileSink2.GetFileDuration","IWMWriterFileSink2::GetFileDuration","IWMWriterFileSink2GetFileDuration","wmformat.iwmwriterfilesink2_getfileduration","wmsdkidl/IWMWriterFileSink2::GetFileDuration"]
old-location: wmformat\iwmwriterfilesink2_getfileduration.htm
tech.root: wmformat
ms.assetid: b0685760-929d-4c65-84e0-a9745635eddd
ms.date: 4/26/2023
ms.keywords: GetFileDuration, GetFileDuration method [windows Media Format], GetFileDuration method [windows Media Format],IWMWriterFileSink2 interface, IWMWriterFileSink2 interface [windows Media Format],GetFileDuration method, IWMWriterFileSink2.GetFileDuration, IWMWriterFileSink2::GetFileDuration, IWMWriterFileSink2GetFileDuration, wmformat.iwmwriterfilesink2_getfileduration, wmsdkidl/IWMWriterFileSink2::GetFileDuration
req.header: wmsdkidl.h
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
 - IWMWriterFileSink2::GetFileDuration
 - wmsdkidl/IWMWriterFileSink2::GetFileDuration
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
 - IWMWriterFileSink2.GetFileDuration
---

# IWMWriterFileSink2::GetFileDuration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetFileDuration</b> method retrieves the duration of the portion of the file that has been written.

## -parameters

### -param pcnsDuration [out]

Pointer to variable specifying the duration, in 100-nanosecond units.

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
The <i>pcnsDuration</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>