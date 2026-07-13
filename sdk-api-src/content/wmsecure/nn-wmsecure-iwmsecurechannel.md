---
UID: NN:wmsecure.IWMSecureChannel
title: IWMSecureChannel (wmsecure.h)
description: The IWMSecureChannel interface provides methods that allow two DLLs to validate each other and perform secure communication.
helpviewer_keywords: ["IWMSecureChannel","IWMSecureChannel interface [windows Media Format]","IWMSecureChannel interface [windows Media Format]","described","wmformat.iwmsecurechannel","wmsecure/IWMSecureChannel"]
old-location: wmformat\iwmsecurechannel.htm
tech.root: wmformat
ms.assetid: ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5
ms.date: 4/26/2023
ms.keywords: IWMSecureChannel, IWMSecureChannel interface [windows Media Format], IWMSecureChannel interface [windows Media Format],described, wmformat.iwmsecurechannel, wmsecure/IWMSecureChannel
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSecureChannel
 - wmsecure/IWMSecureChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel
---

# IWMSecureChannel interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMSecureChannel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>IWMSecureChannel</b> interface provides methods that allow two DLLs to validate
 each other and perform secure communication.

## -inheritance

The <b>IWMSecureChannel</b> interface inherits from <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmauthorizer">IWMAuthorizer</a>. <b>IWMSecureChannel</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmauthorizer">IWMAuthorizer</a>
