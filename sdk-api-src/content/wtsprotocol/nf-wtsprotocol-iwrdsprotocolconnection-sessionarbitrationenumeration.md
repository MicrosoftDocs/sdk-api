---
UID: NF:wtsprotocol.IWRdsProtocolConnection.SessionArbitrationEnumeration
title: IWRdsProtocolConnection::SessionArbitrationEnumeration (wtsprotocol.h)
description: Called after arbitration to allow the protocol to specify the sessions to be reconnected.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","SessionArbitrationEnumeration method","IWRdsProtocolConnection.SessionArbitrationEnumeration","IWRdsProtocolConnection::SessionArbitrationEnumeration","SessionArbitrationEnumeration","SessionArbitrationEnumeration method [Remote Desktop Services]","SessionArbitrationEnumeration method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_sessionarbitrationenumeration","wtsprotocol/IWRdsProtocolConnection::SessionArbitrationEnumeration"]
old-location: termserv\iwrdsprotocolconnection_sessionarbitrationenumeration.htm
tech.root: TermServ
ms.assetid: d0e93014-1f79-47ac-bf3a-c100eb652751
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],SessionArbitrationEnumeration method, IWRdsProtocolConnection.SessionArbitrationEnumeration, IWRdsProtocolConnection::SessionArbitrationEnumeration, SessionArbitrationEnumeration, SessionArbitrationEnumeration method [Remote Desktop Services], SessionArbitrationEnumeration method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_sessionarbitrationenumeration, wtsprotocol/IWRdsProtocolConnection::SessionArbitrationEnumeration
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
 - IWRdsProtocolConnection::SessionArbitrationEnumeration
 - wtsprotocol/IWRdsProtocolConnection::SessionArbitrationEnumeration
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
 - IWRdsProtocolConnection.SessionArbitrationEnumeration
---

# IWRdsProtocolConnection::SessionArbitrationEnumeration


## -description

Called after arbitration to allow the protocol to specify the sessions to be reconnected. The protocol extension should return <b>E_NOTIMPL</b> to use the default session arbitration.

## -parameters

### -param hUserToken [in]

A handle that represents the user token.

### -param bSingleSessionPerUserEnabled [in]

Specifies whether a user can only be associated with a single session.

### -param pSessionIdArray [out]

A pointer to a <b>ULONG</b> array that receives the disconnected session identifiers for the user. If this parameter is <b>NULL</b>, the Remote Desktop Services service is requesting the number of elements to allocate this array. Place the number of identifiers in the value pointed to by <i>pdwSessionIdentifierCount</i>.

### -param pdwSessionIdentifierCount [in, out]

A pointer to a <b>ULONG</b> value that receives the number of elements in the <i>pSessionIdArray</i> array.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>