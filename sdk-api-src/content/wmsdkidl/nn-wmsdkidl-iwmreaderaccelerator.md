---
UID: NN:wmsdkidl.IWMReaderAccelerator
title: IWMReaderAccelerator (wmsdkidl.h)
description: The IWMReaderAccelerator interface is implemented on the reader object only when it is in decoding mode. It is called by a player or a player source filter to obtain interfaces from the decoder DMO.
helpviewer_keywords: ["IWMReaderAccelerator","IWMReaderAccelerator interface [windows Media Format]","IWMReaderAccelerator interface [windows Media Format]","described","IWMReaderAcceleratorInterface","wmformat.iwmreaderaccelerator","wmsdkidl/IWMReaderAccelerator"]
old-location: wmformat\iwmreaderaccelerator.htm
tech.root: wmformat
ms.assetid: cf783b70-4d19-4006-ad0e-e1f883f00b0b
ms.date: 4/26/2023
ms.keywords: IWMReaderAccelerator, IWMReaderAccelerator interface [windows Media Format], IWMReaderAccelerator interface [windows Media Format],described, IWMReaderAcceleratorInterface, wmformat.iwmreaderaccelerator, wmsdkidl/IWMReaderAccelerator
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
 - IWMReaderAccelerator
 - wmsdkidl/IWMReaderAccelerator
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
 - IWMReaderAccelerator
---

# IWMReaderAccelerator interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderAccelerator</b> interface is implemented on the reader object only when it is in decoding mode. It is called by a player or a player source filter to obtain interfaces from the decoder <a href="/windows/desktop/wmformat/wmformat-glossary">DMO</a>.

## -inheritance

The <b>IWMReaderAccelerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderAccelerator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>
