---
UID: NN:wmsdkidl.IWMStreamConfig3
title: IWMStreamConfig3 (wmsdkidl.h)
description: The IWMStreamConfig3 interface controls language settings for a stream.An IWMStreamConfig3 interface exists for every stream configuration object.
helpviewer_keywords: ["IWMStreamConfig3","IWMStreamConfig3 interface [windows Media Format]","IWMStreamConfig3 interface [windows Media Format]","described","IWMStreamConfig3Interface","wmformat.iwmstreamconfig3","wmsdkidl/IWMStreamConfig3"]
old-location: wmformat\iwmstreamconfig3.htm
tech.root: wmformat
ms.assetid: c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681
ms.date: 4/26/2023
ms.keywords: IWMStreamConfig3, IWMStreamConfig3 interface [windows Media Format], IWMStreamConfig3 interface [windows Media Format],described, IWMStreamConfig3Interface, wmformat.iwmstreamconfig3, wmsdkidl/IWMStreamConfig3
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
 - IWMStreamConfig3
 - wmsdkidl/IWMStreamConfig3
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
 - IWMStreamConfig3
---

# IWMStreamConfig3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMStreamConfig3</b> interface controls language settings for a stream.

An <b>IWMStreamConfig3</b> interface exists for every stream configuration object. You can obtain a pointer to an <b>IWMStreamConfig3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the stream configuration object.

## -inheritance

The <b>IWMStreamConfig3</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2</a>. <b>IWMStreamConfig3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
