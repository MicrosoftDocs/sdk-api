---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.OnReady
title: IWTSProtocolConnectionCallback::OnReady (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::OnReady is no longer available. Instead, use IWRdsProtocolConnectionCallback::OnReady.
old-location: termserv\iwtsprotocolconnectioncallback_onready.htm
tech.root: TermServ
ms.assetid: a1289aca-bcf6-4fd2-a288-d401bece005d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],OnReady method, IWTSProtocolConnectionCallback.OnReady, IWTSProtocolConnectionCallback::OnReady, OnReady, OnReady method [Remote Desktop Services], OnReady method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_onready, wtsprotocol/IWTSProtocolConnectionCallback::OnReady
ms.topic: method
f1_keywords: 
 - "wtsprotocol/IWTSProtocolConnectionCallback.OnReady"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnectionCallback.OnReady
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnectionCallback::OnReady


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::OnReady</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnectioncallback-onready">IWRdsProtocolConnectionCallback::OnReady</a>.]

Requests that the Remote Desktop Services service continue the connection process for that client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



The protocol must call this method after the Remote Desktop Services service calls <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a>. The Remote Desktop Services service will not call <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection">AcceptConnection</a> to continue the connection process until <b>OnReady</b> has been called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>
 

 

