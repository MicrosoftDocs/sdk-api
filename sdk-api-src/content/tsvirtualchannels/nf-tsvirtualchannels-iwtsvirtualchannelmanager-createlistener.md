---
UID: NF:tsvirtualchannels.IWTSVirtualChannelManager.CreateListener
title: IWTSVirtualChannelManager::CreateListener (tsvirtualchannels.h)
author: windows-sdk-content
description: Returns an instance of a listener object that listens on a specific endpoint.
old-location: termserv\iwtsvirtualchannelmanager_createlistener.htm
tech.root: TermServ
ms.assetid: 62800999-bd13-4529-b5e4-5c6d67d3a6bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateListener, CreateListener method [Remote Desktop Services], CreateListener method [Remote Desktop Services],IWTSVirtualChannelManager interface, IWTSVirtualChannelManager interface [Remote Desktop Services],CreateListener method, IWTSVirtualChannelManager.CreateListener, IWTSVirtualChannelManager::CreateListener, termserv.iwtsvirtualchannelmanager_createlistener, tsvirtualchannels/IWTSVirtualChannelManager::CreateListener
ms.topic: method
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
 - IWTSVirtualChannelManager.CreateListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Returns a listener callback (<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>)  that will receive notifications for incoming connections.


### -param ppListener [out, optional]

An instance of the <a href="https://msdn.microsoft.com/af0dda9a-0d18-4f44-ac13-0bf2b903d34e">IWTSListener</a> object.


## -returns



Returns <b>S_OK</b> on success.




## -see-also




<a href="https://msdn.microsoft.com/af0dda9a-0d18-4f44-ac13-0bf2b903d34e">IWTSListener</a>



<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>



<a href="https://msdn.microsoft.com/289f76b8-dbb5-4f80-98e9-f39f7946494b">IWTSVirtualChannelManager</a>
 

 

