---
UID: NF:wmsdkidl.IWMWriterPostView.SetReceivePostViewSamples
title: IWMWriterPostView::SetReceivePostViewSamples (wmsdkidl.h)
description: The SetReceivePostViewSamples method enables or disables delivery of postview samples for the specified stream.
helpviewer_keywords: ["IWMWriterPostView interface [windows Media Format]","SetReceivePostViewSamples method","IWMWriterPostView.SetReceivePostViewSamples","IWMWriterPostView::SetReceivePostViewSamples","IWMWriterPostViewSetReceivePostViewSamples","SetReceivePostViewSamples","SetReceivePostViewSamples method [windows Media Format]","SetReceivePostViewSamples method [windows Media Format]","IWMWriterPostView interface","wmformat.iwmwriterpostview_setreceivepostviewsamples","wmsdkidl/IWMWriterPostView::SetReceivePostViewSamples"]
old-location: wmformat\iwmwriterpostview_setreceivepostviewsamples.htm
tech.root: wmformat
ms.assetid: 6d58671a-357b-412b-ad77-61866b0dcce3
ms.date: 12/05/2018
ms.keywords: IWMWriterPostView interface [windows Media Format],SetReceivePostViewSamples method, IWMWriterPostView.SetReceivePostViewSamples, IWMWriterPostView::SetReceivePostViewSamples, IWMWriterPostViewSetReceivePostViewSamples, SetReceivePostViewSamples, SetReceivePostViewSamples method [windows Media Format], SetReceivePostViewSamples method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setreceivepostviewsamples, wmsdkidl/IWMWriterPostView::SetReceivePostViewSamples
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
 - IWMWriterPostView::SetReceivePostViewSamples
 - wmsdkidl/IWMWriterPostView::SetReceivePostViewSamples
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
 - IWMWriterPostView.SetReceivePostViewSamples
---

# IWMWriterPostView::SetReceivePostViewSamples


## -description

The <b>SetReceivePostViewSamples</b> method enables or disables delivery of postview samples for the specified stream.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param fReceivePostViewSamples [in]

Boolean value that is True if postview samples must be delivered.

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
<i>wStreamNum</i> is less than 1 or greater than the maximum number of streams.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
Could not get the output for that stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Stream does not support postview.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples">IWMWriterPostView::GetReceivePostViewSamples</a>