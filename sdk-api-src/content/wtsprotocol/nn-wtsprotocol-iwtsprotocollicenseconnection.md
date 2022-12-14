---
UID: NN:wtsprotocol.IWTSProtocolLicenseConnection
title: IWTSProtocolLicenseConnection (wtsprotocol.h)
description: IWTSProtocolLicenseConnection is no longer available. Instead, use IWRdsProtocolLicenseConnection.
helpviewer_keywords: ["IWTSProtocolLicenseConnection","IWTSProtocolLicenseConnection interface [Remote Desktop Services]","IWTSProtocolLicenseConnection interface [Remote Desktop Services]","described","termserv.iwtsprotocollicenseconnection","wtsprotocol/IWTSProtocolLicenseConnection"]
old-location: termserv\iwtsprotocollicenseconnection.htm
tech.root: TermServ
ms.assetid: 3f6925b6-c712-40c6-8b48-7df8ef4a9872
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLicenseConnection, IWTSProtocolLicenseConnection interface [Remote Desktop Services], IWTSProtocolLicenseConnection interface [Remote Desktop Services],described, termserv.iwtsprotocollicenseconnection, wtsprotocol/IWTSProtocolLicenseConnection
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
 - IWTSProtocolLicenseConnection
 - wtsprotocol/IWTSProtocolLicenseConnection
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
 - IWTSProtocolLicenseConnection
---

# IWTSProtocolLicenseConnection interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a>.]

Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence. This interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.

## -inheritance

The <b>IWTSProtocolLicenseConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolLicenseConnection</b> also has these types of members:

