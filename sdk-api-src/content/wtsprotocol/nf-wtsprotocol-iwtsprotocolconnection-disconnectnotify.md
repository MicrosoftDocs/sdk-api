---
UID: NF:wtsprotocol.IWTSProtocolConnection.DisconnectNotify
title: IWTSProtocolConnection::DisconnectNotify
author: windows-sdk-content
description: IWTSProtocolConnection::DisconnectNotify is no longer available. Instead, use IWRdsProtocolConnection::DisconnectNotify.
old-location: termserv\iwtsprotocolconnection_disconnectnotify.htm
tech.root: termserv
ms.assetid: d2712d53-2e52-49d9-874e-e6425235d3f0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DisconnectNotify, DisconnectNotify method [Remote Desktop Services], DisconnectNotify method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],DisconnectNotify method, IWTSProtocolConnection.DisconnectNotify, IWTSProtocolConnection::DisconnectNotify, termserv.iwtsprotocolconnection_disconnectnotify, wtsprotocol/IWTSProtocolConnection::DisconnectNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.DisconnectNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnection::DisconnectNotify


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::DisconnectNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/2399677b-0859-4e43-9dbc-0b08fa0647b0">IWRdsProtocolConnection::DisconnectNotify</a>.]

Notifies the protocol that the session has been disconnected.


## -parameters






## -remarks



This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

