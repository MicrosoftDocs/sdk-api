---
UID: NF:wtsprotocol.IWRdsProtocolShadowConnection.Stop
title: IWRdsProtocolShadowConnection::Stop (wtsprotocol.h)
description: Notifies the protocol that shadowing has stopped.
old-location: termserv\iwrdsprotocolshadowconnection_stop.htm
tech.root: TermServ
ms.assetid: b6abe698-a390-485a-9a31-823ff25351c2
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowConnection interface [Remote Desktop Services],Stop method, IWRdsProtocolShadowConnection.Stop, IWRdsProtocolShadowConnection::Stop, Stop, Stop method [Remote Desktop Services], Stop method [Remote Desktop Services],IWRdsProtocolShadowConnection interface, termserv.iwrdsprotocolshadowconnection_stop, wtsprotocol/IWRdsProtocolShadowConnection::Stop
ms.topic: method
f1_keywords:
- wtsprotocol/IWRdsProtocolShadowConnection.Stop
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
- IWRdsProtocolShadowConnection.Stop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolShadowConnection::Stop


## -description


Notifies the protocol that shadowing has stopped.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. The Remote Desktop Services service drops the connection if an error is returned.




## -remarks



The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact it is no longer being shadowed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a>
 

 

