---
UID: NF:wtsprotocol.IWTSProtocolConnection.Close
title: IWTSProtocolConnection::Close
author: windows-sdk-content
description: IWTSProtocolConnection::Close is no longer available. Instead, use IWRdsProtocolConnection::Close.
old-location: termserv\iwtsprotocolconnection_close.htm
old-project: TermServ
ms.assetid: 746f5f06-7068-461b-8adf-b35d0c318942
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: Close, Close method [Remote Desktop Services], Close method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],Close method, IWTSProtocolConnection.Close, IWTSProtocolConnection::Close, termserv.iwtsprotocolconnection_close, wtsprotocol/IWTSProtocolConnection::Close
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
 - IWTSProtocolConnection.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::Close


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::Close</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/8d159e3f-b429-4522-b608-0068b1f7fa4e">IWRdsProtocolConnection::Close</a>.]

Closes a connection after the session is disconnected.


## -parameters






## -remarks



 The protocol should perform whatever cleanup is necessary to close the connection and delete the <a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>  object.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

