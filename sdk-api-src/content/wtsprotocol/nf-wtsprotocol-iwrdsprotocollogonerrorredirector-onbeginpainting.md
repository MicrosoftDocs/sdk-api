---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.OnBeginPainting
title: IWRdsProtocolLogonErrorRedirector::OnBeginPainting (wtsprotocol.h)
description: Notifies the protocol that the logon user interface is ready to begin painting.
helpviewer_keywords: ["IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services]","OnBeginPainting method","IWRdsProtocolLogonErrorRedirector.OnBeginPainting","IWRdsProtocolLogonErrorRedirector::OnBeginPainting","OnBeginPainting","OnBeginPainting method [Remote Desktop Services]","OnBeginPainting method [Remote Desktop Services]","IWRdsProtocolLogonErrorRedirector interface","termserv.iwrdsprotocollogonerrorredirector_onbeginpainting","wtsprotocol/IWRdsProtocolLogonErrorRedirector::OnBeginPainting"]
old-location: termserv\iwrdsprotocollogonerrorredirector_onbeginpainting.htm
tech.root: TermServ
ms.assetid: cc044746-1127-44a3-993d-ca2445c99ff6
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],OnBeginPainting method, IWRdsProtocolLogonErrorRedirector.OnBeginPainting, IWRdsProtocolLogonErrorRedirector::OnBeginPainting, OnBeginPainting, OnBeginPainting method [Remote Desktop Services], OnBeginPainting method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, termserv.iwrdsprotocollogonerrorredirector_onbeginpainting, wtsprotocol/IWRdsProtocolLogonErrorRedirector::OnBeginPainting
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
 - IWRdsProtocolLogonErrorRedirector::OnBeginPainting
 - wtsprotocol/IWRdsProtocolLogonErrorRedirector::OnBeginPainting
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
 - IWRdsProtocolLogonErrorRedirector.OnBeginPainting
---

# IWRdsProtocolLogonErrorRedirector::OnBeginPainting


## -description

Notifies the protocol that the logon user interface is ready to begin painting.



## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a>
