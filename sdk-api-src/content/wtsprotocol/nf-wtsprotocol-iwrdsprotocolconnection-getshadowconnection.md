---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetShadowConnection
title: IWRdsProtocolConnection::GetShadowConnection (wtsprotocol.h)
description: Retrieves a reference to the shadow connection object from the protocol.
helpviewer_keywords: ["GetShadowConnection","GetShadowConnection method [Remote Desktop Services]","GetShadowConnection method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetShadowConnection method","IWRdsProtocolConnection.GetShadowConnection","IWRdsProtocolConnection::GetShadowConnection","termserv.iwrdsprotocolconnection_getshadowconnection","wtsprotocol/IWRdsProtocolConnection::GetShadowConnection"]
old-location: termserv\iwrdsprotocolconnection_getshadowconnection.htm
tech.root: TermServ
ms.assetid: 1b1059af-f673-47fd-85fc-57df76adfbcf
ms.date: 12/05/2018
ms.keywords: GetShadowConnection, GetShadowConnection method [Remote Desktop Services], GetShadowConnection method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetShadowConnection method, IWRdsProtocolConnection.GetShadowConnection, IWRdsProtocolConnection::GetShadowConnection, termserv.iwrdsprotocolconnection_getshadowconnection, wtsprotocol/IWRdsProtocolConnection::GetShadowConnection
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
 - IWRdsProtocolConnection::GetShadowConnection
 - wtsprotocol/IWRdsProtocolConnection::GetShadowConnection
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
 - IWRdsProtocolConnection.GetShadowConnection
---

# IWRdsProtocolConnection::GetShadowConnection


## -description

Retrieves a reference to the shadow connection object from the protocol.

## -parameters

### -param ppShadowConnection [out]

The address of <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a> interface pointer that receives the reference to the shadow connection object. This method must add a reference to the object before returning. When the Remote Desktop Services service no longer needs the object, it will release it.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>



<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a>