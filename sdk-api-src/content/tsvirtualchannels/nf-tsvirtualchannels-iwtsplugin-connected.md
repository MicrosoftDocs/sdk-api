---
UID: NF:tsvirtualchannels.IWTSPlugin.Connected
title: IWTSPlugin::Connected (tsvirtualchannels.h)
description: Notifies the plug-in that the Remote Desktop Connection (RDC) client has successfully connected to the Remote Desktop Session Host (RD Session Host) server.
helpviewer_keywords: ["Connected","Connected method [Remote Desktop Services]","Connected method [Remote Desktop Services]","IWTSPlugin interface","IWTSPlugin interface [Remote Desktop Services]","Connected method","IWTSPlugin.Connected","IWTSPlugin::Connected","termserv.iwtsplugin_connected","tsvirtualchannels/IWTSPlugin::Connected"]
old-location: termserv\iwtsplugin_connected.htm
tech.root: TermServ
ms.assetid: 089db67e-6c3d-4950-a1dd-de0a3bbe8d5c
ms.date: 12/05/2018
ms.keywords: Connected, Connected method [Remote Desktop Services], Connected method [Remote Desktop Services],IWTSPlugin interface, IWTSPlugin interface [Remote Desktop Services],Connected method, IWTSPlugin.Connected, IWTSPlugin::Connected, termserv.iwtsplugin_connected, tsvirtualchannels/IWTSPlugin::Connected
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSPlugin::Connected
 - tsvirtualchannels/IWTSPlugin::Connected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSPlugin.Connected
---

# IWTSPlugin::Connected


## -description

Notifies the plug-in that the Remote Desktop Connection (RDC) client has successfully connected to the Remote Desktop Session Host (RD Session Host) server.



## -returns

Returns <b>S_OK</b> if the call completes successfully. Returns <b>E_FAIL</b> if the call fails, but the plug-in will continue to work.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsplugin">IWTSPlugin</a>
