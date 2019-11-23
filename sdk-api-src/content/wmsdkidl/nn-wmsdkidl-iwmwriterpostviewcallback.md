---
UID: NN:wmsdkidl.IWMWriterPostViewCallback
title: IWMWriterPostViewCallback (wmsdkidl.h)

description: The IWMWriterPostViewCallback interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.This interface must be implemented by the application and passed to IWMWriterPostView::SetPostViewCallback.
old-location: wmformat\iwmwriterpostviewcallback.htm
tech.root: wmformat
ms.assetid: 987dd3b4-2245-4640-820c-5a9660ab5e37

ms.date: 12/05/2018
ms.keywords: IWMWriterPostViewCallback, IWMWriterPostViewCallback interface [windows Media Format], IWMWriterPostViewCallback interface [windows Media Format],described, IWMWriterPostViewCallbackInterface, wmformat.iwmwriterpostviewcallback, wmsdkidl/IWMWriterPostViewCallback
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMWriterPostViewCallback"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterPostViewCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterPostViewCallback interface


## -description



The <b>IWMWriterPostViewCallback</b> interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.

This interface must be implemented by the application and passed to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback">IWMWriterPostView::SetPostViewCallback</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPostViewCallback</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a>. <b>IWMWriterPostViewCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPostViewCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-allocateforpostview">AllocateForPostView</a>
</td>
<td align="left" width="63%">
Allocates a buffer for use in postviewing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample">OnPostViewSample</a>
</td>
<td align="left" width="63%">
Called when new postview data is available.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/to-use-writer-postview">To Use Writer Postview</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

