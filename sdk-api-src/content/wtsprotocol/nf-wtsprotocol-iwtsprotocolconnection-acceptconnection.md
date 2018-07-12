---
UID: NF:wtsprotocol.IWTSProtocolConnection.AcceptConnection
title: IWTSProtocolConnection::AcceptConnection
author: windows-sdk-content
description: IWTSProtocolConnection::AcceptConnection is no longer available. Instead, use IWRdsProtocolConnection::AcceptConnection.
old-location: termserv\iwtsprotocolconnection_acceptconnection.htm
old-project: TermServ
ms.assetid: 5be00911-f68a-410d-8d56-81458b5ff44e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AcceptConnection, AcceptConnection method [Remote Desktop Services], AcceptConnection method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],AcceptConnection method, IWTSProtocolConnection.AcceptConnection, IWTSProtocolConnection::AcceptConnection, termserv.iwtsprotocolconnection_acceptconnection, wtsprotocol/IWTSProtocolConnection::AcceptConnection
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.AcceptConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::AcceptConnection


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::AcceptConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/ef7e13ad-eeb8-4452-b3d6-a137b766f98f">IWRdsProtocolConnection::AcceptConnection</a>.]

Directs the protocol to continue with the connection request.


## -parameters






## -remarks



During a connection sequence, the Remote Desktop Services service calls this method after it receives a connection request from a client and after it calls the <a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a> method.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

