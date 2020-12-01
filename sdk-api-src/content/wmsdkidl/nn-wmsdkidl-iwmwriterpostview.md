---
UID: NN:wmsdkidl.IWMWriterPostView
title: IWMWriterPostView (wmsdkidl.h)
description: The IWMWriterPostView interface manages advanced writing functionality related to the postviewing of samples.
helpviewer_keywords: ["IWMWriterPostView","IWMWriterPostView interface [windows Media Format]","IWMWriterPostView interface [windows Media Format]","described","IWMWriterPostViewInterface","wmformat.iwmwriterpostview","wmsdkidl/IWMWriterPostView"]
old-location: wmformat\iwmwriterpostview.htm
tech.root: wmformat
ms.assetid: 1d24dbd6-86df-4a0a-8110-15f6a4c1f31d
ms.date: 12/05/2018
ms.keywords: IWMWriterPostView, IWMWriterPostView interface [windows Media Format], IWMWriterPostView interface [windows Media Format],described, IWMWriterPostViewInterface, wmformat.iwmwriterpostview, wmsdkidl/IWMWriterPostView
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterPostView
 - wmsdkidl/IWMWriterPostView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterPostView
---

# IWMWriterPostView interface


## -description

The <b>IWMWriterPostView</b> interface manages advanced writing functionality related to the postviewing of samples. Postviewing displays the media samples as a viewer of the ASF file would see them, and is often used after encoding to check the output. Postviewing is supported only for video.

This interface can be obtained from any interface on the writer object by calling <b>QueryInterface</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPostView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterPostView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPostView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getallocateforpostview">GetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Ascertains whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewformat">GetPostViewFormat</a>
</td>
<td align="left" width="63%">
Retrieves the media properties for the specified output stream and output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewformatcount">GetPostViewFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of possible output formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getpostviewprops">GetPostViewProps</a>
</td>
<td align="left" width="63%">
Retrieves the properties for the specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples">GetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether delivery of postview samples is enabled for the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setallocateforpostview">SetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Specifies whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback">SetPostViewCallback</a>
</td>
<td align="left" width="63%">
Specifies the callback interface to use for receiving postview samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewprops">SetPostViewProps</a>
</td>
<td align="left" width="63%">
Specifies the properties for the output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples">SetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Enables or disables delivery of postview samples for the specified stream.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="/windows/desktop/wmformat/writer-object">Writer Object</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/to-use-writer-postview">To Use Writer Postview</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>