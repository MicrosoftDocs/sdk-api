---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetClientMonitorData
title: IWRdsProtocolConnection::GetClientMonitorData (wtsprotocol.h)
description: Retrieves the number of monitors and the primary monitor number on the client.
helpviewer_keywords: ["GetClientMonitorData","GetClientMonitorData method [Remote Desktop Services]","GetClientMonitorData method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetClientMonitorData method","IWRdsProtocolConnection.GetClientMonitorData","IWRdsProtocolConnection::GetClientMonitorData","termserv.iwrdsprotocolconnection_getclientmonitordata","termserv.iwrdsremotefxgraphicsconnection_getclientmonitordata","wtsprotocol/IWRdsProtocolConnection::GetClientMonitorData"]
old-location: termserv\iwrdsprotocolconnection_getclientmonitordata.htm
tech.root: TermServ
ms.assetid: df70ff56-3e12-4842-a818-31ee75da96a9
ms.date: 12/05/2018
ms.keywords: GetClientMonitorData, GetClientMonitorData method [Remote Desktop Services], GetClientMonitorData method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetClientMonitorData method, IWRdsProtocolConnection.GetClientMonitorData, IWRdsProtocolConnection::GetClientMonitorData, termserv.iwrdsprotocolconnection_getclientmonitordata, termserv.iwrdsremotefxgraphicsconnection_getclientmonitordata, wtsprotocol/IWRdsProtocolConnection::GetClientMonitorData
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
 - IWRdsProtocolConnection::GetClientMonitorData
 - wtsprotocol/IWRdsProtocolConnection::GetClientMonitorData
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
 - IWRdsProtocolConnection.GetClientMonitorData
---

# IWRdsProtocolConnection::GetClientMonitorData


## -description

Retrieves the number of monitors and the primary monitor number on the client.

## -parameters

### -param pNumMonitors [out]

A pointer to a <b>UINT</b> variable to receive the number of monitors counted.

### -param pPrimaryMonitor [out]

A pointer to a <b>UINT</b> variable to receive the number of the primary monitor on the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>