---
UID: NF:wmpservices.IWMPPlugin.Shutdown
title: IWMPPlugin::Shutdown (wmpservices.h)
description: The IWMPPlugin::Shutdown method is called when Windows Media Player shuts down the plug-in.
helpviewer_keywords: ["IWMPPlugin interface [Windows Media Player]","Shutdown method","IWMPPlugin.Shutdown","IWMPPlugin::Shutdown","IWMPPluginShutdownDSP","Shutdown","Shutdown method [Windows Media Player]","Shutdown method [Windows Media Player]","IWMPPlugin interface","wmp.iwmpplugin_shutdown","wmpservices/IWMPPlugin::Shutdown"]
old-location: wmp\iwmpplugin_shutdown.htm
tech.root: WMP
ms.assetid: 80a8fe19-3660-49cb-8bbb-0267b3f11b63
ms.date: 4/26/2023
ms.keywords: IWMPPlugin interface [Windows Media Player],Shutdown method, IWMPPlugin.Shutdown, IWMPPlugin::Shutdown, IWMPPluginShutdownDSP, Shutdown, Shutdown method [Windows Media Player], Shutdown method [Windows Media Player],IWMPPlugin interface, wmp.iwmpplugin_shutdown, wmpservices/IWMPPlugin::Shutdown
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPPlugin::Shutdown
 - wmpservices/IWMPPlugin::Shutdown
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
 - IWMPPlugin.Shutdown
---

# IWMPPlugin::Shutdown


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlugin::Shutdown</b> method is called when Windows Media Player shuts down the plug-in.



## -returns

The method returns an <b>HRESULT</b>.

## -remarks

<b>Init</b> and <b>Shutdown</b> will always be called on the same thread.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>
