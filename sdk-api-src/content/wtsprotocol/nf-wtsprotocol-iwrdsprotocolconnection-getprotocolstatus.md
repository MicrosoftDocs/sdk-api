---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetProtocolStatus
title: IWRdsProtocolConnection::GetProtocolStatus (wtsprotocol.h)
description: Retrieves information about the protocol status.
helpviewer_keywords: ["GetProtocolStatus","GetProtocolStatus method [Remote Desktop Services]","GetProtocolStatus method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetProtocolStatus method","IWRdsProtocolConnection.GetProtocolStatus","IWRdsProtocolConnection::GetProtocolStatus","termserv.iwrdsprotocolconnection_getprotocolstatus","wtsprotocol/IWRdsProtocolConnection::GetProtocolStatus"]
old-location: termserv\iwrdsprotocolconnection_getprotocolstatus.htm
tech.root: TermServ
ms.assetid: A89C2E3F-AC75-4CFB-9DA7-00DCEDCA1C1A
ms.date: 12/05/2018
ms.keywords: GetProtocolStatus, GetProtocolStatus method [Remote Desktop Services], GetProtocolStatus method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetProtocolStatus method, IWRdsProtocolConnection.GetProtocolStatus, IWRdsProtocolConnection::GetProtocolStatus, termserv.iwrdsprotocolconnection_getprotocolstatus, wtsprotocol/IWRdsProtocolConnection::GetProtocolStatus
f1_keywords:
- wtsprotocol/IWRdsProtocolConnection.GetProtocolStatus
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolConnection::GetProtocolStatus


## -description


Retrieves information about the protocol status.


## -parameters




### -param pProtocolStatus [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_protocol_status">WRDS_PROTOCOL_STATUS</a> structure that receives counter, signal, and cache information for the protocol.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>
 

 

