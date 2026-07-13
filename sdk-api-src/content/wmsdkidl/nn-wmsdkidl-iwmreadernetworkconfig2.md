---
UID: NN:wmsdkidl.IWMReaderNetworkConfig2
title: IWMReaderNetworkConfig2 (wmsdkidl.h)
description: The IWMReaderNetworkConfig2 interface provides advanced networking functionality.An IWMReaderNetworkConfig2 interface exists for every reader object.
helpviewer_keywords: ["IWMReaderNetworkConfig2","IWMReaderNetworkConfig2 interface [windows Media Format]","IWMReaderNetworkConfig2 interface [windows Media Format]","described","IWMReaderNetworkConfig2Interface","wmformat.iwmreadernetworkconfig2","wmsdkidl/IWMReaderNetworkConfig2"]
old-location: wmformat\iwmreadernetworkconfig2.htm
tech.root: wmformat
ms.assetid: a0480243-53e0-4da5-a119-291b19f46951
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], IWMReaderNetworkConfig2 interface [windows Media Format],described, IWMReaderNetworkConfig2Interface, wmformat.iwmreadernetworkconfig2, wmsdkidl/IWMReaderNetworkConfig2
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
 - IWMReaderNetworkConfig2
 - wmsdkidl/IWMReaderNetworkConfig2
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
 - IWMReaderNetworkConfig2
---

# IWMReaderNetworkConfig2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderNetworkConfig2</b> interface provides advanced networking functionality.

An <b>IWMReaderNetworkConfig2</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMReaderNetworkConfig2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig</a>. <b>IWMReaderNetworkConfig2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
