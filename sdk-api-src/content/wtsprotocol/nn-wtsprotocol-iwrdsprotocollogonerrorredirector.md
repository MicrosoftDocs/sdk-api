---
UID: NN:wtsprotocol.IWRdsProtocolLogonErrorRedirector
title: IWRdsProtocolLogonErrorRedirector (wtsprotocol.h)
description: Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.
helpviewer_keywords: ["IWRdsProtocolLogonErrorRedirector","IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services]","IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services]","described","termserv.iwrdsprotocollogonerrorredirector","wtsprotocol/IWRdsProtocolLogonErrorRedirector"]
old-location: termserv\iwrdsprotocollogonerrorredirector.htm
tech.root: TermServ
ms.assetid: 43c283f5-c902-49cc-81a0-15fc6316c7d4
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector, IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services], IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],described, termserv.iwrdsprotocollogonerrorredirector, wtsprotocol/IWRdsProtocolLogonErrorRedirector
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
 - IWRdsProtocolLogonErrorRedirector
 - wtsprotocol/IWRdsProtocolLogonErrorRedirector
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
 - IWRdsProtocolLogonErrorRedirector
---

# IWRdsProtocolLogonErrorRedirector interface


## -description

Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages. This interface is implemented by the protocol.

## -inheritance

The <b>IWRdsProtocolLogonErrorRedirector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolLogonErrorRedirector</b> also has these types of members:

## -remarks

To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.
