---
UID: NF:wtsprotocol.IWTSProtocolConnection.SendPolicyData
title: IWTSProtocolConnection::SendPolicyData method
author: windows-driver-content
description: IWTSProtocolConnection::SendPolicyData is no longer available. Instead, use IWRdsProtocolManager::NotifySettingsChange.
old-location: termserv\iwtsprotocolconnection_sendpolicydata.htm
old-project: TermServ
ms.assetid: b3fcc213-8257-433f-b304-ce19bc209591
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], SendPolicyData method, IWTSProtocolConnection::SendPolicyData, SendPolicyData method [Remote Desktop Services], SendPolicyData method [Remote Desktop Services], IWTSProtocolConnection interface, SendPolicyData,IWTSProtocolConnection.SendPolicyData, termserv.iwtsprotocolconnection_sendpolicydata, wtsprotocol/IWTSProtocolConnection::SendPolicyData
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
-	IWTSProtocolConnection.SendPolicyData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::SendPolicyData method


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SendPolicyData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/80292d9b-fced-4726-8f83-5ba355df06a2">IWRdsProtocolManager::NotifySettingsChange</a>.]

Sends computer policy settings to the custom protocol. These settings are a combination of listener policies and Group Policy settings.


## -parameters




### -param pPolicyData [in]

A pointer to a <a href="https://msdn.microsoft.com/407de671-f6e3-407e-9c97-11ea9ac8bdde">WTS_POLICY_DATA</a> structure that contains computer policy settings.


## -remarks



The <b>SendPolicyData</b> method is the second method called by the Remote Desktop Services service during a connection sequence.  The protocol must call the <a href="https://msdn.microsoft.com/a1289aca-bcf6-4fd2-a288-d401bece005d">OnReady</a> method after this method is called, or the connection is dropped. 




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

