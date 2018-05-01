---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetLogonErrorRedirector
title: IWTSProtocolConnection::GetLogonErrorRedirector method
author: windows-driver-content
description: IWTSProtocolConnection::GetLogonErrorRedirector is no longer available. Instead, use IWRdsProtocolConnection::GetLogonErrorRedirector.
old-location: termserv\iwtsprotocolconnection_getlogonerrorredirector.htm
old-project: TermServ
ms.assetid: 59bd7d50-2903-42b7-b556-4da7b50d8e7a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetLogonErrorRedirector method [Remote Desktop Services], GetLogonErrorRedirector method [Remote Desktop Services], IWTSProtocolConnection interface, GetLogonErrorRedirector,IWTSProtocolConnection.GetLogonErrorRedirector, IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], GetLogonErrorRedirector method, IWTSProtocolConnection::GetLogonErrorRedirector, termserv.iwtsprotocolconnection_getlogonerrorredirector, wtsprotocol/IWTSProtocolConnection::GetLogonErrorRedirector
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
-	IWTSProtocolConnection.GetLogonErrorRedirector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::GetLogonErrorRedirector method


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetLogonErrorRedirector</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/9613330F-B8DE-48C7-892C-FB8F50739C13">IWRdsProtocolConnection::GetLogonErrorRedirector</a>.]

Retrieves an <a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors. The protocol must add a reference to this object before returning, and the Remote Desktop Services service releases the reference when the connection is closed.


## -parameters




### -param ppLogonErrorRedir [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a> interface.


## -remarks



The <a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a> interface is implemented by the protocol to receive status and error messages from the Remote Desktop Services service.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

