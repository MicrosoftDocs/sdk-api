---
UID: NF:wmsdkidl.IWMWriterPostView.GetAllocateForPostView
title: IWMWriterPostView::GetAllocateForPostView (wmsdkidl.h)
description: The GetAllocateForPostView method ascertains whether the application, and not the writer, must supply the buffers.
helpviewer_keywords: ["GetAllocateForPostView","GetAllocateForPostView method [windows Media Format]","GetAllocateForPostView method [windows Media Format]","IWMWriterPostView interface","IWMWriterPostView interface [windows Media Format]","GetAllocateForPostView method","IWMWriterPostView.GetAllocateForPostView","IWMWriterPostView::GetAllocateForPostView","IWMWriterPostViewGetAllocateForPostView","wmformat.iwmwriterpostview_getallocateforpostview","wmsdkidl/IWMWriterPostView::GetAllocateForPostView"]
old-location: wmformat\iwmwriterpostview_getallocateforpostview.htm
tech.root: wmformat
ms.assetid: bd17eeec-a1ce-42db-a807-008ca2c4194f
ms.date: 4/26/2023
ms.keywords: GetAllocateForPostView, GetAllocateForPostView method [windows Media Format], GetAllocateForPostView method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetAllocateForPostView method, IWMWriterPostView.GetAllocateForPostView, IWMWriterPostView::GetAllocateForPostView, IWMWriterPostViewGetAllocateForPostView, wmformat.iwmwriterpostview_getallocateforpostview, wmsdkidl/IWMWriterPostView::GetAllocateForPostView
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
 - IWMWriterPostView::GetAllocateForPostView
 - wmsdkidl/IWMWriterPostView::GetAllocateForPostView
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
 - IWMWriterPostView.GetAllocateForPostView
---

# IWMWriterPostView::GetAllocateForPostView


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAllocateForPostView</b> method ascertains whether the application, and not the writer, must supply the buffers.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param pfAllocate [out]

Pointer to Boolean value that is True if the application allocates buffers, and False if this is left to the writer.

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
NULL value passed in to <i>pfAllocate</i>.

</td>
</tr>
</table>

## -remarks

See the Remarks for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setallocateforpostview">SetAllocateForPostView</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>