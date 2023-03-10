---
UID: NF:wmsdkidl.IWMWriterPostView.GetReceivePostViewSamples
title: IWMWriterPostView::GetReceivePostViewSamples (wmsdkidl.h)
description: The GetReceivePostViewSamples method retrieves a flag indicating whether delivery of postview samples has been turned on for the specified stream.
helpviewer_keywords: ["GetReceivePostViewSamples","GetReceivePostViewSamples method [windows Media Format]","GetReceivePostViewSamples method [windows Media Format]","IWMWriterPostView interface","IWMWriterPostView interface [windows Media Format]","GetReceivePostViewSamples method","IWMWriterPostView.GetReceivePostViewSamples","IWMWriterPostView::GetReceivePostViewSamples","IWMWriterPostViewGetReceivePostViewSamples","wmformat.iwmwriterpostview_getreceivepostviewsamples","wmsdkidl/IWMWriterPostView::GetReceivePostViewSamples"]
old-location: wmformat\iwmwriterpostview_getreceivepostviewsamples.htm
tech.root: wmformat
ms.assetid: 93120e68-2d1c-4628-8e2e-d22a56fa98a3
ms.date: 12/05/2018
ms.keywords: GetReceivePostViewSamples, GetReceivePostViewSamples method [windows Media Format], GetReceivePostViewSamples method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetReceivePostViewSamples method, IWMWriterPostView.GetReceivePostViewSamples, IWMWriterPostView::GetReceivePostViewSamples, IWMWriterPostViewGetReceivePostViewSamples, wmformat.iwmwriterpostview_getreceivepostviewsamples, wmsdkidl/IWMWriterPostView::GetReceivePostViewSamples
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
 - IWMWriterPostView::GetReceivePostViewSamples
 - wmsdkidl/IWMWriterPostView::GetReceivePostViewSamples
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
 - IWMWriterPostView.GetReceivePostViewSamples
---

# IWMWriterPostView::GetReceivePostViewSamples


## -description

The <b>GetReceivePostViewSamples</b> method retrieves a flag indicating whether delivery of postview samples has been turned on for the specified stream.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param pfReceivePostViewSamples [out]

Pointer to a flag; True indicates that postview samples are to be delivered.

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
NULL value passed to <i>pfReceivePostViewSamples</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples">IWMWriterPostView::SetReceivePostViewSamples</a>