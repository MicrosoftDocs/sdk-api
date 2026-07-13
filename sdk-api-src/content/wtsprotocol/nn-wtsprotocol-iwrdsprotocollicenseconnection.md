---
UID: NN:wtsprotocol.IWRdsProtocolLicenseConnection
title: IWRdsProtocolLicenseConnection (wtsprotocol.h)
description: Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.
helpviewer_keywords: ["IWRdsProtocolLicenseConnection","IWRdsProtocolLicenseConnection interface [Remote Desktop Services]","IWRdsProtocolLicenseConnection interface [Remote Desktop Services]","described","termserv.iwrdsprotocollicenseconnection","wtsprotocol/IWRdsProtocolLicenseConnection"]
old-location: termserv\iwrdsprotocollicenseconnection.htm
tech.root: TermServ
ms.assetid: 498c31c5-1cb6-41d7-91fb-7409ea03dda0
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection, IWRdsProtocolLicenseConnection interface [Remote Desktop Services], IWRdsProtocolLicenseConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocollicenseconnection, wtsprotocol/IWRdsProtocolLicenseConnection
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
 - IWRdsProtocolLicenseConnection
 - wtsprotocol/IWRdsProtocolLicenseConnection
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
 - IWRdsProtocolLicenseConnection
---

# IWRdsProtocolLicenseConnection interface


## -description

Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence. This interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.

## -inheritance

The <b>IWRdsProtocolLicenseConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolLicenseConnection</b> also has these types of members:

## -remarks

To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.
