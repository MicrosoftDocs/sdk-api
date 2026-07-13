---
UID: NF:wmsdkidl.IWMWriterPostView.GetPostViewFormat
title: IWMWriterPostView::GetPostViewFormat (wmsdkidl.h)
description: The GetPostViewFormat method retrieves the media properties for the specified output stream and output format.
helpviewer_keywords: ["GetPostViewFormat","GetPostViewFormat method [windows Media Format]","GetPostViewFormat method [windows Media Format]","IWMWriterPostView interface","IWMWriterPostView interface [windows Media Format]","GetPostViewFormat method","IWMWriterPostView.GetPostViewFormat","IWMWriterPostView::GetPostViewFormat","IWMWriterPostViewGetPostViewFormat","wmformat.iwmwriterpostview_getpostviewformat","wmsdkidl/IWMWriterPostView::GetPostViewFormat"]
old-location: wmformat\iwmwriterpostview_getpostviewformat.htm
tech.root: wmformat
ms.assetid: 3636833d-3c96-45d9-bf82-e3ff930c7d9b
ms.date: 4/26/2023
ms.keywords: GetPostViewFormat, GetPostViewFormat method [windows Media Format], GetPostViewFormat method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetPostViewFormat method, IWMWriterPostView.GetPostViewFormat, IWMWriterPostView::GetPostViewFormat, IWMWriterPostViewGetPostViewFormat, wmformat.iwmwriterpostview_getpostviewformat, wmsdkidl/IWMWriterPostView::GetPostViewFormat
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
 - IWMWriterPostView::GetPostViewFormat
 - wmsdkidl/IWMWriterPostView::GetPostViewFormat
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
 - IWMWriterPostView.GetPostViewFormat
---

# IWMWriterPostView::GetPostViewFormat


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPostViewFormat</b> method retrieves the media properties for the specified output stream and output format.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param dwFormatNumber [in]

<b>DWORD</b> containing the format number.

### -param ppProps [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a> interface.

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
NULL value passed in to <i>ppProps</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete the task.

</td>
</tr>
</table>

## -remarks

This method can be used along with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewformatcount">GetPostViewFormatCount</a> to determine all possible format types supported by this output on the reader.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>