---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetShadowConnection
title: IWTSProtocolConnection::GetShadowConnection method
author: windows-driver-content
description: IWTSProtocolConnection::GetShadowConnection is no longer available. Instead, use IWRdsProtocolConnection::GetShadowConnection.
old-location: termserv\iwtsprotocolconnection_getshadowconnection.htm
old-project: TermServ
ms.assetid: 6496deba-6166-48d2-9294-286a448de231
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetShadowConnection method [Remote Desktop Services], GetShadowConnection method [Remote Desktop Services], IWTSProtocolConnection interface, GetShadowConnection,IWTSProtocolConnection.GetShadowConnection, IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], GetShadowConnection method, IWTSProtocolConnection::GetShadowConnection, termserv.iwtsprotocolconnection_getshadowconnection, wtsprotocol/IWTSProtocolConnection::GetShadowConnection
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolConnection.GetShadowConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::GetShadowConnection method


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetShadowConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/1b1059af-f673-47fd-85fc-57df76adfbcf">IWRdsProtocolConnection::GetShadowConnection</a>.]

Retrieves a  <a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a> object from the protocol. The method must add a reference to the object before returning. When the Remote Desktop Services service has finished the licensing process, it will release the reference.


## -parameters




### -param ppShadowConnection [out]

 The address of a pointer to an <a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

