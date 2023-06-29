---
UID: NF:wmsdkidl.IWMWriterPostView.SetPostViewProps
title: IWMWriterPostView::SetPostViewProps (wmsdkidl.h)
description: The SetPostViewProps method specifies the format for the specified output stream.
helpviewer_keywords: ["IWMWriterPostView interface [windows Media Format]","SetPostViewProps method","IWMWriterPostView.SetPostViewProps","IWMWriterPostView::SetPostViewProps","IWMWriterPostViewSetPostViewProps","SetPostViewProps","SetPostViewProps method [windows Media Format]","SetPostViewProps method [windows Media Format]","IWMWriterPostView interface","wmformat.iwmwriterpostview_setpostviewprops","wmsdkidl/IWMWriterPostView::SetPostViewProps"]
old-location: wmformat\iwmwriterpostview_setpostviewprops.htm
tech.root: wmformat
ms.assetid: e5b92065-fff3-41d2-b263-375ae14869e5
ms.date: 4/26/2023
ms.keywords: IWMWriterPostView interface [windows Media Format],SetPostViewProps method, IWMWriterPostView.SetPostViewProps, IWMWriterPostView::SetPostViewProps, IWMWriterPostViewSetPostViewProps, SetPostViewProps, SetPostViewProps method [windows Media Format], SetPostViewProps method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setpostviewprops, wmsdkidl/IWMWriterPostView::SetPostViewProps
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
 - IWMWriterPostView::SetPostViewProps
 - wmsdkidl/IWMWriterPostView::SetPostViewProps
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
 - IWMWriterPostView.SetPostViewProps
---

# IWMWriterPostView::SetPostViewProps


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetPostViewProps</b> method specifies the format for the specified output stream.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param pOutput [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a> interface.

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
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The stream number specified by <i>wStreamNumber</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to create an internal structure.

</td>
</tr>
</table>

## -remarks

It is not possible to resize the video output using postview properties.

<b>SetPostViewProps</b> fails if <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a> has been called. If any postview properties need to be changed, this should be done before calling <b>BeginWriting</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewprops">IWMWriterPostView::GetPostViewProps</a>