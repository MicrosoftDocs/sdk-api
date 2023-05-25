---
UID: NN:wmpservices.IWMPUserEventSink
title: IWMPUserEventSink (wmpservices.h)
description: The IWMPUserEventSink interface receives event notifications from a custom video presenter.
helpviewer_keywords: ["IWMPUserEventSink","IWMPUserEventSink interface [Windows Media Player]","IWMPUserEventSink interface [Windows Media Player]","described","IWMPUserEventSinkInterface","wmp.iwmpusereventsink","wmpservices/IWMPUserEventSink"]
old-location: wmp\iwmpusereventsink.htm
tech.root: WMP
ms.assetid: b9afa601-543e-4338-a603-2fe4cd56db36
ms.date: 4/26/2023
ms.keywords: IWMPUserEventSink, IWMPUserEventSink interface [Windows Media Player], IWMPUserEventSink interface [Windows Media Player],described, IWMPUserEventSinkInterface, wmp.iwmpusereventsink, wmpservices/IWMPUserEventSink
req.header: wmpservices.h
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
 - IWMPUserEventSink
 - wmpservices/IWMPUserEventSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPUserEventSink
---

# IWMPUserEventSink interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPUserEventSink</b> interface receives event notifications from a custom video presenter. An application that embeds the Windows Media Player control, and provides a custom video presenter, can implement the <b>IWMPUserEventSink</b> interface.

The Windows Media Player control retrieves a pointer to the application's <b>IWMPUserEventSink</b> interface by calling <b>IServiceProvider::QueryService</b>, passing __uuidof(IWMPUserEventSink) in the <i>riid</i> parameter. Therefore, an application that implements the <b>IWMPUserEventSink</b> interface must also implement the <b>IServiceProvider</b> interface.

## -inheritance

The <b>IWMPUserEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPUserEventSink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>
