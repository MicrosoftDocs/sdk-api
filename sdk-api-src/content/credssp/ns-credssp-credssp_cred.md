---
UID: NS:credssp._CREDSSP_CRED
title: CREDSSP_CRED (credssp.h)
description: Specifies authentication data for both Schannel and Negotiate security packages.
helpviewer_keywords: ["*PCREDSSP_CRED","CREDSSP_CRED","CREDSSP_CRED structure [Security]","PCREDSSP_CRED","PCREDSSP_CRED structure pointer [Security]","credssp/CREDSSP_CRED","credssp/PCREDSSP_CRED","security.credssp_cred"]
old-location: security\credssp_cred.htm
tech.root: security
ms.assetid: b22bd22c-e6e1-4817-b5cf-ab49f574e75f
ms.date: 12/05/2018
ms.keywords: '*PCREDSSP_CRED, CREDSSP_CRED, CREDSSP_CRED structure [Security], PCREDSSP_CRED, PCREDSSP_CRED structure pointer [Security], credssp/CREDSSP_CRED, credssp/PCREDSSP_CRED, security.credssp_cred'
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
targetos: Windows
req.typenames: CREDSSP_CRED, *PCREDSSP_CRED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDSSP_CRED
 - credssp/_CREDSSP_CRED
 - PCREDSSP_CRED
 - credssp/PCREDSSP_CRED
 - CREDSSP_CRED
 - credssp/CREDSSP_CRED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credssp.h
api_name:
 - CREDSSP_CRED
---

# CREDSSP_CRED structure


## -description

 The <b>CREDSSP_CRED</b> structure specifies authentication data for both Schannel and Negotiate <a href="/windows/desktop/SecGloss/s-gly">security packages</a>.

## -struct-fields

### -field Type

The <a href="/windows/win32/api/credssp/ne-credssp-credspp_submit_type">CREDSPP_SUBMIT_TYPE</a> enumeration value that specifies the type of credentials contained in this structure.

### -field pSchannelCred

A pointer to a set of Schannel credentials.

### -field pSpnegoCred

A pointer to a set of Negotiate credentials.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (CredSSP)</a>



<a href="/windows/win32/api/credssp/ne-credssp-credspp_submit_type">CREDSPP_SUBMIT_TYPE</a>