---
UID: NE:credssp._CREDSSP_SUBMIT_TYPE
title: CREDSPP_SUBMIT_TYPE (credssp.h)
description: Specifies the type of credentials specified by a CREDSSP_CRED structure.
helpviewer_keywords: ["CREDSPP_SUBMIT_TYPE","CREDSPP_SUBMIT_TYPE enumeration [Security]","CredsspCertificateCreds","CredsspPasswordCreds","CredsspSchannelCreds","CredsspSubmitBufferBoth","CredsspSubmitBufferBothOld","credssp/CREDSPP_SUBMIT_TYPE","credssp/CredsspCertificateCreds","credssp/CredsspPasswordCreds","credssp/CredsspSchannelCreds","credssp/CredsspSubmitBufferBoth","credssp/CredsspSubmitBufferBothOld","security.credspp_submit_type"]
old-location: security\credspp_submit_type.htm
tech.root: security
ms.assetid: d30e219b-ea39-41da-b714-3ceb13a5614d
ms.date: 12/05/2018
ms.keywords: CREDSPP_SUBMIT_TYPE, CREDSPP_SUBMIT_TYPE enumeration [Security], CredsspCertificateCreds, CredsspPasswordCreds, CredsspSchannelCreds, CredsspSubmitBufferBoth, CredsspSubmitBufferBothOld, credssp/CREDSPP_SUBMIT_TYPE, credssp/CredsspCertificateCreds, credssp/CredsspPasswordCreds, credssp/CredsspSchannelCreds, credssp/CredsspSubmitBufferBoth, credssp/CredsspSubmitBufferBothOld, security.credspp_submit_type
f1_keywords:
- credssp/CREDSPP_SUBMIT_TYPE
dev_langs:
- c++
req.header: credssp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- HeaderDef
api_location:
- Credssp.h
api_name:
- CREDSPP_SUBMIT_TYPE
targetos: Windows
req.typenames: CREDSPP_SUBMIT_TYPE
req.redist: 
ms.custom: 19H1
---

# CREDSPP_SUBMIT_TYPE enumeration


## -description


The <b>CREDSPP_SUBMIT_TYPE</b> enumeration specifies the type of credentials specified by a <a href="https://docs.microsoft.com/windows/desktop/api/credssp/ns-credssp-credssp_cred">CREDSSP_CRED</a> structure.


## -enum-fields




### -field CredsspPasswordCreds

The credentials are a user name and password.


### -field CredsspSchannelCreds

The credentials are Schannel credentials.


### -field CredsspCertificateCreds

The credentials are in a certificate.


### -field CredsspSubmitBufferBoth

The credentials contain both certificate and Schannel credentials.


### -field CredsspSubmitBufferBothOld


### -field CredsspCredEx




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credssp/ns-credssp-credssp_cred">CREDSSP_CRED</a>
 

 

