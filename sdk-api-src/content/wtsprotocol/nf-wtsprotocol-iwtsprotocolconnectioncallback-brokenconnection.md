---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.BrokenConnection
title: IWTSProtocolConnectionCallback::BrokenConnection (wtsprotocol.h)
description: IWTSProtocolConnectionCallback::BrokenConnection is no longer available. Instead, use IWRdsProtocolConnectionCallback::BrokenConnection.
helpviewer_keywords: ["BrokenConnection","BrokenConnection method [Remote Desktop Services]","BrokenConnection method [Remote Desktop Services]","IWTSProtocolConnectionCallback interface","IWTSProtocolConnectionCallback interface [Remote Desktop Services]","BrokenConnection method","IWTSProtocolConnectionCallback.BrokenConnection","IWTSProtocolConnectionCallback::BrokenConnection","termserv.iwtsprotocolconnectioncallback_brokenconnection","wtsprotocol/IWTSProtocolConnectionCallback::BrokenConnection"]
old-location: termserv\iwtsprotocolconnectioncallback_brokenconnection.htm
tech.root: TermServ
ms.assetid: a5878289-9335-4b3b-b66a-4c168b868f87
ms.date: 12/05/2018
ms.keywords: BrokenConnection, BrokenConnection method [Remote Desktop Services], BrokenConnection method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, IWTSProtocolConnectionCallback interface [Remote Desktop Services],BrokenConnection method, IWTSProtocolConnectionCallback.BrokenConnection, IWTSProtocolConnectionCallback::BrokenConnection, termserv.iwtsprotocolconnectioncallback_brokenconnection, wtsprotocol/IWTSProtocolConnectionCallback::BrokenConnection
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
 - IWTSProtocolConnectionCallback::BrokenConnection
 - wtsprotocol/IWTSProtocolConnectionCallback::BrokenConnection
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
 - IWTSProtocolConnectionCallback.BrokenConnection
---

# IWTSProtocolConnectionCallback::BrokenConnection


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::BrokenConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnectioncallback-brokenconnection">IWRdsProtocolConnectionCallback::BrokenConnection</a>.]

Informs the Remote Desktop Services service that the client connection has been lost.

## -parameters

### -param Reason [in]

This parameter is not used.

### -param Source [in]

This parameter is not used.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>