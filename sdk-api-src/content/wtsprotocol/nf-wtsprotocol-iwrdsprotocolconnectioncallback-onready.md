---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.OnReady
title: IWRdsProtocolConnectionCallback::OnReady (wtsprotocol.h)
description: Requests that the Remote Desktop Services service continue the connection process for that client.helpviewer_keywords: ["IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","OnReady method","IWRdsProtocolConnectionCallback.OnReady","IWRdsProtocolConnectionCallback::OnReady","OnReady","OnReady method [Remote Desktop Services]","OnReady method [Remote Desktop Services]","IWRdsProtocolConnectionCallback interface","termserv.iwrdsprotocolconnectioncallback_onready","wtsprotocol/IWRdsProtocolConnectionCallback::OnReady"]
old-location: termserv\iwrdsprotocolconnectioncallback_onready.htm
tech.root: TermServ
ms.assetid: 88134a34-c494-48ea-9063-206e7d0c5139
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],OnReady method, IWRdsProtocolConnectionCallback.OnReady, IWRdsProtocolConnectionCallback::OnReady, OnReady, OnReady method [Remote Desktop Services], OnReady method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_onready, wtsprotocol/IWRdsProtocolConnectionCallback::OnReady
f1_keywords:
- wtsprotocol/IWRdsProtocolConnectionCallback.OnReady
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
- IWRdsProtocolConnectionCallback.OnReady
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolConnectionCallback::OnReady


## -description


Requests that the Remote Desktop Services service continue the connection process for that client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



The protocol must call this method after the Remote Desktop Services service calls <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>. The Remote Desktop Services service will not call <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-acceptconnection">AcceptConnection</a> to continue the connection process until <b>OnReady</b> has been called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>
 

 

