---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetClientData
title: IWTSProtocolConnection::GetClientData (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::GetClientData is no longer available. Instead, use IWRdsProtocolConnection::GetClientData.
old-location: termserv\iwtsprotocolconnection_getclientdata.htm
tech.root: TermServ
ms.assetid: 1330fbb4-4c10-493b-ad95-3c2ad975459a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClientData, GetClientData method [Remote Desktop Services], GetClientData method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetClientData method, IWTSProtocolConnection.GetClientData, IWTSProtocolConnection::GetClientData, termserv.iwtsprotocolconnection_getclientdata, wtsprotocol/IWTSProtocolConnection::GetClientData
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
 - IWTSProtocolConnection.GetClientData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnection::GetClientData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetClientData</b> 
    is no longer available for use as of Windows Server 2012. Instead, use 
    <a href="https://msdn.microsoft.com/4005ff92-56ea-46ae-a546-e08a80303ef5">IWRdsProtocolConnection::GetClientData</a>.]

Requests client settings from the protocol.


## -parameters




### -param pClientData [out]

A pointer to a <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WTS_CLIENT_DATA</a> structure that contains the client settings.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

