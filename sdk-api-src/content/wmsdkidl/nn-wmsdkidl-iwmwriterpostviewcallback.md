---
UID: NN:wmsdkidl.IWMWriterPostViewCallback
title: IWMWriterPostViewCallback (wmsdkidl.h)
description: The IWMWriterPostViewCallback interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.This interface must be implemented by the application and passed to IWMWriterPostView::SetPostViewCallback.
helpviewer_keywords: ["IWMWriterPostViewCallback","IWMWriterPostViewCallback interface [windows Media Format]","IWMWriterPostViewCallback interface [windows Media Format]","described","IWMWriterPostViewCallbackInterface","wmformat.iwmwriterpostviewcallback","wmsdkidl/IWMWriterPostViewCallback"]
old-location: wmformat\iwmwriterpostviewcallback.htm
tech.root: wmformat
ms.assetid: 987dd3b4-2245-4640-820c-5a9660ab5e37
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterPostViewCallback</b> interface manages the receiving of uncompressed samples from the writer. Postview can be used only for video streams.

This interface must be implemented by the application and passed to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback">IWMWriterPostView::SetPostViewCallback</a>.

## -inheritance

The <b>IWMWriterPostViewCallback</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a>. <b>IWMWriterPostViewCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/to-use-writer-postview">To Use Writer Postview</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
