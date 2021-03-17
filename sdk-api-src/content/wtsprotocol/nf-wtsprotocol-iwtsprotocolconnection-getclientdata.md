---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetClientData
title: IWTSProtocolConnection::GetClientData (wtsprotocol.h)
description: IWTSProtocolConnection::GetClientData is no longer available. Instead, use IWRdsProtocolConnection::GetClientData.
helpviewer_keywords: ["GetClientData","GetClientData method [Remote Desktop Services]","GetClientData method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetClientData method","IWTSProtocolConnection.GetClientData","IWTSProtocolConnection::GetClientData","termserv.iwtsprotocolconnection_getclientdata","wtsprotocol/IWTSProtocolConnection::GetClientData"]
old-location: termserv\iwtsprotocolconnection_getclientdata.htm
tech.root: TermServ
ms.assetid: 1330fbb4-4c10-493b-ad95-3c2ad975459a
ms.date: 12/05/2018
ms.keywords: GetClientData, GetClientData method [Remote Desktop Services], GetClientData method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetClientData method, IWTSProtocolConnection.GetClientData, IWTSProtocolConnection::GetClientData, termserv.iwtsprotocolconnection_getclientdata, wtsprotocol/IWTSProtocolConnection::GetClientData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection::GetClientData
 - wtsprotocol/IWTSProtocolConnection::GetClientData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.GetClientData
---

# IWTSProtocolConnection::GetClientData


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetClientData</b> 
    is no longer available for use as of Windows Server 2012. Instead, use 
    <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getclientdata">IWRdsProtocolConnection::GetClientData</a>.]

Requests client settings from the protocol.

## -parameters

### -param pClientData [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_client_data">WTS_CLIENT_DATA</a> structure that contains the client settings.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>