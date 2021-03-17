---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetClientData
title: IWRdsProtocolConnection::GetClientData (wtsprotocol.h)
description: Requests client settings from the protocol.
helpviewer_keywords: ["GetClientData","GetClientData method [Remote Desktop Services]","GetClientData method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetClientData method","IWRdsProtocolConnection.GetClientData","IWRdsProtocolConnection::GetClientData","termserv.iwrdsprotocolconnection_getclientdata","wtsprotocol/IWRdsProtocolConnection::GetClientData"]
old-location: termserv\iwrdsprotocolconnection_getclientdata.htm
tech.root: TermServ
ms.assetid: 4005ff92-56ea-46ae-a546-e08a80303ef5
ms.date: 12/05/2018
ms.keywords: GetClientData, GetClientData method [Remote Desktop Services], GetClientData method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetClientData method, IWRdsProtocolConnection.GetClientData, IWRdsProtocolConnection::GetClientData, termserv.iwrdsprotocolconnection_getclientdata, wtsprotocol/IWRdsProtocolConnection::GetClientData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolConnection::GetClientData
 - wtsprotocol/IWRdsProtocolConnection::GetClientData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetClientData
---

# IWRdsProtocolConnection::GetClientData


## -description

Requests client settings from the protocol.

## -parameters

### -param pClientData [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_client_data">WRDS_CLIENT_DATA</a> structure that contains the client settings.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

Upon receiving an error, the Remote Desktop Services service will drop the connection.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>