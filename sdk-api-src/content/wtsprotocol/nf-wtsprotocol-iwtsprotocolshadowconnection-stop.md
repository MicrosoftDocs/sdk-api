---
UID: NF:wtsprotocol.IWTSProtocolShadowConnection.Stop
title: IWTSProtocolShadowConnection::Stop (wtsprotocol.h)
description: IWTSProtocolShadowConnection::Stop is no longer available. Instead, use IWRdsProtocolShadowConnection::Stop.
helpviewer_keywords: ["IWTSProtocolShadowConnection interface [Remote Desktop Services]","Stop method","IWTSProtocolShadowConnection.Stop","IWTSProtocolShadowConnection::Stop","Stop","Stop method [Remote Desktop Services]","Stop method [Remote Desktop Services]","IWTSProtocolShadowConnection interface","termserv.iwtsprotocolshadowconnection_stop","wtsprotocol/IWTSProtocolShadowConnection::Stop"]
old-location: termserv\iwtsprotocolshadowconnection_stop.htm
tech.root: TermServ
ms.assetid: 629b82cb-7bf3-4a83-bc96-a1e6a757f974
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowConnection interface [Remote Desktop Services],Stop method, IWTSProtocolShadowConnection.Stop, IWTSProtocolShadowConnection::Stop, Stop, Stop method [Remote Desktop Services], Stop method [Remote Desktop Services],IWTSProtocolShadowConnection interface, termserv.iwtsprotocolshadowconnection_stop, wtsprotocol/IWTSProtocolShadowConnection::Stop
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
 - IWTSProtocolShadowConnection::Stop
 - wtsprotocol/IWTSProtocolShadowConnection::Stop
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
 - IWTSProtocolShadowConnection.Stop
---

# IWTSProtocolShadowConnection::Stop


## -description

<p class="CCE_Message">[<b>IWTSProtocolShadowConnection::Stop</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowconnection-stop">IWRdsProtocolShadowConnection::Stop</a>.]

Notifies the protocol that shadowing has stopped.



## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. The Remote Desktop Services service drops the connection if an error is returned.

## -remarks

The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact it is no longer being shadowed.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a>
