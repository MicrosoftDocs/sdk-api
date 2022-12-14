---
UID: NF:wmpservices.IWMPPlugin.Shutdown
title: IWMPPlugin::Shutdown (wmpservices.h)
description: The IWMPPlugin::Shutdown method is called when Windows Media Player shuts down the plug-in.
helpviewer_keywords: ["IWMPPlugin interface [Windows Media Player]","Shutdown method","IWMPPlugin.Shutdown","IWMPPlugin::Shutdown","IWMPPluginShutdownDSP","Shutdown","Shutdown method [Windows Media Player]","Shutdown method [Windows Media Player]","IWMPPlugin interface","wmp.iwmpplugin_shutdown","wmpservices/IWMPPlugin::Shutdown"]
old-location: wmp\iwmpplugin_shutdown.htm
tech.root: WMP
ms.assetid: 80a8fe19-3660-49cb-8bbb-0267b3f11b63
ms.date: 12/05/2018
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

The <b>IWMPPlugin::Shutdown</b> method is called when Windows Media Player shuts down the plug-in.



## -returns

The method returns an <b>HRESULT</b>.

## -remarks

<b>Init</b> and <b>Shutdown</b> will always be called on the same thread.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>
