---
UID: NN:wmsdkidl.IWMWriterPostViewCallback
title: IWMWriterPostViewCallback (wmsdkidl.h)
description: The IWMWriterPostViewCallback interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.This interface must be implemented by the application and passed to IWMWriterPostView::SetPostViewCallback.
helpviewer_keywords: ["IWMWriterPostViewCallback","IWMWriterPostViewCallback interface [windows Media Format]","IWMWriterPostViewCallback interface [windows Media Format]","described","IWMWriterPostViewCallbackInterface","wmformat.iwmwriterpostviewcallback","wmsdkidl/IWMWriterPostViewCallback"]
old-location: wmformat\iwmwriterpostviewcallback.htm
tech.root: wmformat
ms.assetid: 987dd3b4-2245-4640-820c-5a9660ab5e37
ms.date: 12/05/2018
ms.keywords: IWMWriterPostViewCallback, IWMWriterPostViewCallback interface [windows Media Format], IWMWriterPostViewCallback interface [windows Media Format],described, IWMWriterPostViewCallbackInterface, wmformat.iwmwriterpostviewcallback, wmsdkidl/IWMWriterPostViewCallback
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
 - IWMWriterPostViewCallback
 - wmsdkidl/IWMWriterPostViewCallback
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
 - IWMWriterPostViewCallback
---

# IWMWriterPostViewCallback interface


## -description

The <b>IWMWriterPostViewCallback</b> interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.

This interface must be implemented by the application and passed to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback">IWMWriterPostView::SetPostViewCallback</a>.

## -inheritance

The <b>IWMWriterPostViewCallback</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a>. <b>IWMWriterPostViewCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/to-use-writer-postview">To Use Writer Postview</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
