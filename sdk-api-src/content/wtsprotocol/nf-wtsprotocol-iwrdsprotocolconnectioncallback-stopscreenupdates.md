---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.StopScreenUpdates
title: IWRdsProtocolConnectionCallback::StopScreenUpdates (wtsprotocol.h)
description: Requests that the Remote Desktop Services service stop updating the client screen.helpviewer_keywords: ["IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","StopScreenUpdates method","IWRdsProtocolConnectionCallback.StopScreenUpdates","IWRdsProtocolConnectionCallback::StopScreenUpdates","StopScreenUpdates","StopScreenUpdates method [Remote Desktop Services]","StopScreenUpdates method [Remote Desktop Services]","IWRdsProtocolConnectionCallback interface","termserv.iwrdsprotocolconnectioncallback_stopscreenupdates","wtsprotocol/IWRdsProtocolConnectionCallback::StopScreenUpdates"]
old-location: termserv\iwrdsprotocolconnectioncallback_stopscreenupdates.htm
tech.root: TermServ
ms.assetid: 698b59d3-8391-4101-801c-8d5fd701a757
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],StopScreenUpdates method, IWRdsProtocolConnectionCallback.StopScreenUpdates, IWRdsProtocolConnectionCallback::StopScreenUpdates, StopScreenUpdates, StopScreenUpdates method [Remote Desktop Services], StopScreenUpdates method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_stopscreenupdates, wtsprotocol/IWRdsProtocolConnectionCallback::StopScreenUpdates
f1_keywords:
- wtsprotocol/IWRdsProtocolConnectionCallback.StopScreenUpdates
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
- IWRdsProtocolConnectionCallback.StopScreenUpdates
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolConnectionCallback::StopScreenUpdates


## -description


Requests that the Remote Desktop Services service stop updating the client screen.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>
 

 

