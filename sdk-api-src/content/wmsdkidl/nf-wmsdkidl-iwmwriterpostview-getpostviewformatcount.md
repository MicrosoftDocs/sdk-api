---
UID: NF:wmsdkidl.IWMWriterPostView.GetPostViewFormatCount
title: IWMWriterPostView::GetPostViewFormatCount (wmsdkidl.h)
description: The GetPostViewFormatCount method is used for ascertaining all possible format types supported for the specified stream.
helpviewer_keywords: ["GetPostViewFormatCount","GetPostViewFormatCount method [windows Media Format]","GetPostViewFormatCount method [windows Media Format]","IWMWriterPostView interface","IWMWriterPostView interface [windows Media Format]","GetPostViewFormatCount method","IWMWriterPostView.GetPostViewFormatCount","IWMWriterPostView::GetPostViewFormatCount","IWMWriterPostViewGetPostViewFormatCount","wmformat.iwmwriterpostview_getpostviewformatcount","wmsdkidl/IWMWriterPostView::GetPostViewFormatCount"]
old-location: wmformat\iwmwriterpostview_getpostviewformatcount.htm
tech.root: wmformat
ms.assetid: b34b2418-5ae4-49a2-913a-bb4ac604ac4e
ms.date: 4/26/2023
ms.keywords: GetPostViewFormatCount, GetPostViewFormatCount method [windows Media Format], GetPostViewFormatCount method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetPostViewFormatCount method, IWMWriterPostView.GetPostViewFormatCount, IWMWriterPostView::GetPostViewFormatCount, IWMWriterPostViewGetPostViewFormatCount, wmformat.iwmwriterpostview_getpostviewformatcount, wmsdkidl/IWMWriterPostView::GetPostViewFormatCount
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
 - IWMWriterPostView::GetPostViewFormatCount
 - wmsdkidl/IWMWriterPostView::GetPostViewFormatCount
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
 - IWMWriterPostView.GetPostViewFormatCount
---

# IWMWriterPostView::GetPostViewFormatCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPostViewFormatCount</b> method is used for ascertaining all possible format types supported for the specified stream.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param pcFormats [out]

Pointer to a count of the output formats.

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
NULL value passed in to <i>pcFormats</i>.

</td>
</tr>
</table>

## -remarks

This method can be used along with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewformat">GetPostViewFormat</a> to ascertain all possible format types supported by this output on the reader.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>