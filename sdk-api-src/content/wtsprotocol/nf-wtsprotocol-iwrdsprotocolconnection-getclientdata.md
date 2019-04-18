---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetClientData
title: IWRdsProtocolConnection::GetClientData (wtsprotocol.h)
author: windows-sdk-content
description: Requests client settings from the protocol.
old-location: termserv\iwrdsprotocolconnection_getclientdata.htm
tech.root: TermServ
ms.assetid: 4005ff92-56ea-46ae-a546-e08a80303ef5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClientData, GetClientData method [Remote Desktop Services], GetClientData method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetClientData method, IWRdsProtocolConnection.GetClientData, IWRdsProtocolConnection::GetClientData, termserv.iwrdsprotocolconnection_getclientdata, wtsprotocol/IWRdsProtocolConnection::GetClientData
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetClientData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolConnection::GetClientData


## -description


Requests client settings from the protocol.


## -parameters




### -param pClientData [out]

A pointer to a <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WRDS_CLIENT_DATA</a> structure that contains the client settings.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

Upon receiving an error, the Remote Desktop Services service will drop the connection. 




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

