---
UID: NF:wtsprotocol.IWRdsProtocolListenerCallback.OnConnected
title: IWRdsProtocolListenerCallback::OnConnected (wtsprotocol.h)
description: Notifies the Remote Desktop Services service that a client connection request has been received.
helpviewer_keywords: ["IWRdsProtocolListenerCallback interface [Remote Desktop Services]","OnConnected method","IWRdsProtocolListenerCallback.OnConnected","IWRdsProtocolListenerCallback::OnConnected","OnConnected","OnConnected method [Remote Desktop Services]","OnConnected method [Remote Desktop Services]","IWRdsProtocolListenerCallback interface","termserv.iwrdsprotocollistenercallback_onconnected","wtsprotocol/IWRdsProtocolListenerCallback::OnConnected"]
old-location: termserv\iwrdsprotocollistenercallback_onconnected.htm
tech.root: TermServ
ms.assetid: 9d2d5393-f0a6-40ec-9bf2-2e8c945693db
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolListenerCallback interface [Remote Desktop Services],OnConnected method, IWRdsProtocolListenerCallback.OnConnected, IWRdsProtocolListenerCallback::OnConnected, OnConnected, OnConnected method [Remote Desktop Services], OnConnected method [Remote Desktop Services],IWRdsProtocolListenerCallback interface, termserv.iwrdsprotocollistenercallback_onconnected, wtsprotocol/IWRdsProtocolListenerCallback::OnConnected
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
 - IWRdsProtocolListenerCallback::OnConnected
 - wtsprotocol/IWRdsProtocolListenerCallback::OnConnected
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
 - IWRdsProtocolListenerCallback.OnConnected
---

# IWRdsProtocolListenerCallback::OnConnected


## -description

Notifies the Remote Desktop Services service that a client connection request has been received. 
 After this method is called, the Remote Desktop Services service begins the client connection sequence.

## -parameters

### -param pConnection [in]

A pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a> interface that represents a client connection. The Remote Desktop Services service  adds a reference to this object and releases it when it closes the connection.

### -param pWRdsConnectionSettings [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings">WRDS_CONNECTION_SETTINGS</a> structure that contains the connection settings for the remote session.

### -param pCallback [out]

The address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a> interface used by the protocol to notify the Remote Desktop Services service about the status of a client connection. The Remote Desktop Services service  adds a reference to this object and the protocol must release it when the connection is closed.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback">IWRdsProtocolListenerCallback</a>