---
UID: NF:tsvirtualchannels.IWTSVirtualChannelManager.CreateListener
title: IWTSVirtualChannelManager::CreateListener (tsvirtualchannels.h)
description: Returns an instance of a listener object that listens on a specific endpoint.
helpviewer_keywords: ["CreateListener","CreateListener method [Remote Desktop Services]","CreateListener method [Remote Desktop Services]","IWTSVirtualChannelManager interface","IWTSVirtualChannelManager interface [Remote Desktop Services]","CreateListener method","IWTSVirtualChannelManager.CreateListener","IWTSVirtualChannelManager::CreateListener","termserv.iwtsvirtualchannelmanager_createlistener","tsvirtualchannels/IWTSVirtualChannelManager::CreateListener"]
old-location: termserv\iwtsvirtualchannelmanager_createlistener.htm
tech.root: TermServ
ms.assetid: 62800999-bd13-4529-b5e4-5c6d67d3a6bc
ms.date: 12/05/2018
ms.keywords: CreateListener, CreateListener method [Remote Desktop Services], CreateListener method [Remote Desktop Services],IWTSVirtualChannelManager interface, IWTSVirtualChannelManager interface [Remote Desktop Services],CreateListener method, IWTSVirtualChannelManager.CreateListener, IWTSVirtualChannelManager::CreateListener, termserv.iwtsvirtualchannelmanager_createlistener, tsvirtualchannels/IWTSVirtualChannelManager::CreateListener
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
 - IWTSVirtualChannelManager::CreateListener
 - tsvirtualchannels/IWTSVirtualChannelManager::CreateListener
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
 - IWTSVirtualChannelManager.CreateListener
---

# IWTSVirtualChannelManager::CreateListener


## -description

Returns an instance of a listener object that listens on a specific endpoint.

## -parameters

### -param pszChannelName [in]

The endpoint name on which the listener will listen. This is a string value, the length of which is limited to <b>MAX_PATH</b> number of characters.

### -param uFlags [in]

This parameter is reserved and must be set to zero.

### -param pListenerCallback [in, optional]

Returns a listener callback (<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistenercallback">IWTSListenerCallback</a>)  that will receive notifications for incoming connections.

### -param ppListener [out, optional]

An instance of the <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistener">IWTSListener</a> object.

## -returns

Returns <b>S_OK</b> on success.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistener">IWTSListener</a>



<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistenercallback">IWTSListenerCallback</a>



<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager">IWTSVirtualChannelManager</a>