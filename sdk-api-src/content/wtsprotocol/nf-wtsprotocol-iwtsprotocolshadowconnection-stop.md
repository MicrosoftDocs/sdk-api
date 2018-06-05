---
UID: NF:wtsprotocol.IWTSProtocolShadowConnection.Stop
title: IWTSProtocolShadowConnection::Stop
author: windows-sdk-content
description: IWTSProtocolShadowConnection::Stop is no longer available. Instead, use IWRdsProtocolShadowConnection::Stop.
old-location: termserv\iwtsprotocolshadowconnection_stop.htm
old-project: TermServ
ms.assetid: 629b82cb-7bf3-4a83-bc96-a1e6a757f974
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSProtocolShadowConnection interface [Remote Desktop Services],Stop method, IWTSProtocolShadowConnection.Stop, IWTSProtocolShadowConnection::Stop, Stop, Stop method [Remote Desktop Services], Stop method [Remote Desktop Services],IWTSProtocolShadowConnection interface, termserv.iwtsprotocolshadowconnection_stop, wtsprotocol/IWTSProtocolShadowConnection::Stop
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolShadowConnection.Stop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolShadowConnection::Stop


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowConnection::Stop</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/b6abe698-a390-485a-9a31-823ff25351c2">IWRdsProtocolShadowConnection::Stop</a>.]

Notifies the protocol that shadowing has stopped.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. The Remote Desktop Services service drops the connection if an error is returned.




## -remarks



The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact it is no longer being shadowed.




## -see-also




<a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a>
 

 

