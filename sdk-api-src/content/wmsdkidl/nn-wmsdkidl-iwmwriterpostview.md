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

The <b>IWMWriterPostView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterPostView</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/to-use-writer-postview">To Use Writer Postview</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
