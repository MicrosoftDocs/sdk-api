---
UID: NF:tsvirtualchannels.IWTSPlugin.Disconnected
title: IWTSPlugin::Disconnected (tsvirtualchannels.h)
description: Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\iwtsplugin_disconnected.htm
tech.root: TermServ
ms.assetid: cbc753b4-531f-476e-8743-b8fbf2481c91
ms.date: 12/05/2018
ms.keywords: Disconnected, Disconnected method [Remote Desktop Services], Disconnected method [Remote Desktop Services],IWTSPlugin interface, IWTSPlugin interface [Remote Desktop Services],Disconnected method, IWTSPlugin.Disconnected, IWTSPlugin::Disconnected, termserv.iwtsplugin_disconnected, tsvirtualchannels/IWTSPlugin::Disconnected
ms.topic: method
f1_keywords:
- tsvirtualchannels/IWTSPlugin.Disconnected
dev_langs:
- c++
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- TsVirtualChannels.h
api_name:
- IWTSPlugin.Disconnected
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSPlugin::Disconnected


## -description


Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param dwDisconnectCode [in]

Code that identifies the disconnect reason. For the possible codes, see <a href="https://docs.microsoft.com/windows/desktop/TermServ/imstscaxevents-ondisconnected">IMsTscAxEvents::OnDisconnected</a>.


## -returns



Returns <b>S_OK</b> if the call completes successfully. Results in no action if the call fails.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsplugin">IWTSPlugin</a>
 

 

