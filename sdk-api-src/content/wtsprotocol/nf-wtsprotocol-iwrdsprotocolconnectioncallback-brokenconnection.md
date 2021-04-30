---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.BrokenConnection
title: IWRdsProtocolConnectionCallback::BrokenConnection (wtsprotocol.h)
description: Informs the Remote Desktop Services service that the client connection has been lost.
helpviewer_keywords: ["BrokenConnection","BrokenConnection method [Remote Desktop Services]","BrokenConnection method [Remote Desktop Services]","IWRdsProtocolConnectionCallback interface","IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","BrokenConnection method","IWRdsProtocolConnectionCallback.BrokenConnection","IWRdsProtocolConnectionCallback::BrokenConnection","termserv.iwrdsprotocolconnectioncallback_brokenconnection","wtsprotocol/IWRdsProtocolConnectionCallback::BrokenConnection"]
old-location: termserv\iwrdsprotocolconnectioncallback_brokenconnection.htm
tech.root: TermServ
ms.assetid: bc317e10-e09c-423b-8016-eb1cf49eba43
ms.date: 12/05/2018
ms.keywords: BrokenConnection, BrokenConnection method [Remote Desktop Services], BrokenConnection method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, IWRdsProtocolConnectionCallback interface [Remote Desktop Services],BrokenConnection method, IWRdsProtocolConnectionCallback.BrokenConnection, IWRdsProtocolConnectionCallback::BrokenConnection, termserv.iwrdsprotocolconnectioncallback_brokenconnection, wtsprotocol/IWRdsProtocolConnectionCallback::BrokenConnection
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
 - IWRdsProtocolConnectionCallback::BrokenConnection
 - wtsprotocol/IWRdsProtocolConnectionCallback::BrokenConnection
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
 - IWRdsProtocolConnectionCallback.BrokenConnection
---

# IWRdsProtocolConnectionCallback::BrokenConnection


## -description

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

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>