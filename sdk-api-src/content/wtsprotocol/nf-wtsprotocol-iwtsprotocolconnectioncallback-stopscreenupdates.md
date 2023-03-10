---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.StopScreenUpdates
title: IWTSProtocolConnectionCallback::StopScreenUpdates (wtsprotocol.h)
description: IWTSProtocolConnectionCallback::StopScreenUpdates is no longer available. Instead, use IWRdsProtocolConnectionCallback::StopScreenUpdates.
helpviewer_keywords: ["IWTSProtocolConnectionCallback interface [Remote Desktop Services]","StopScreenUpdates method","IWTSProtocolConnectionCallback.StopScreenUpdates","IWTSProtocolConnectionCallback::StopScreenUpdates","StopScreenUpdates","StopScreenUpdates method [Remote Desktop Services]","StopScreenUpdates method [Remote Desktop Services]","IWTSProtocolConnectionCallback interface","termserv.iwtsprotocolconnectioncallback_stopscreenupdates","wtsprotocol/IWTSProtocolConnectionCallback::StopScreenUpdates"]
old-location: termserv\iwtsprotocolconnectioncallback_stopscreenupdates.htm
tech.root: TermServ
ms.assetid: 69fab470-8763-405e-96f1-d3b1c5a26422
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],StopScreenUpdates method, IWTSProtocolConnectionCallback.StopScreenUpdates, IWTSProtocolConnectionCallback::StopScreenUpdates, StopScreenUpdates, StopScreenUpdates method [Remote Desktop Services], StopScreenUpdates method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_stopscreenupdates, wtsprotocol/IWTSProtocolConnectionCallback::StopScreenUpdates
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
 - IWTSProtocolConnectionCallback::StopScreenUpdates
 - wtsprotocol/IWTSProtocolConnectionCallback::StopScreenUpdates
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
 - IWTSProtocolConnectionCallback.StopScreenUpdates
---

# IWTSProtocolConnectionCallback::StopScreenUpdates


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::StopScreenUpdates</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnectioncallback-stopscreenupdates">IWRdsProtocolConnectionCallback::StopScreenUpdates</a>.]

Requests that the Remote Desktop Services service stop updating the client screen.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>
