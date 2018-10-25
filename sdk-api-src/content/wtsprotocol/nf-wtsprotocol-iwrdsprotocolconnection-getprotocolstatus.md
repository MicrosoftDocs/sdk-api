---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetProtocolStatus
title: IWRdsProtocolConnection::GetProtocolStatus
author: windows-sdk-content
description: Retrieves information about the protocol status.
old-location: termserv\iwrdsprotocolconnection_getprotocolstatus.htm
tech.root: termserv
ms.assetid: A89C2E3F-AC75-4CFB-9DA7-00DCEDCA1C1A
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetProtocolStatus, GetProtocolStatus method [Remote Desktop Services], GetProtocolStatus method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetProtocolStatus method, IWRdsProtocolConnection.GetProtocolStatus, IWRdsProtocolConnection::GetProtocolStatus, termserv.iwrdsprotocolconnection_getprotocolstatus, wtsprotocol/IWRdsProtocolConnection::GetProtocolStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWRdsProtocolConnection.GetProtocolStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnection::GetProtocolStatus


## -description


Retrieves information about the protocol status.


## -parameters




### -param pProtocolStatus [out]

A pointer to a <a href="https://msdn.microsoft.com/20e66033-fc79-49c9-af0e-abaf6e4ba501">WRDS_PROTOCOL_STATUS</a> structure that receives counter, signal, and cache information for the protocol.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

