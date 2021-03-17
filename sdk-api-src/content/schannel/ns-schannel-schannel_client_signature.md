---
UID: NS:schannel._SCHANNEL_CLIENT_SIGNATURE
title: SCHANNEL_CLIENT_SIGNATURE (schannel.h)
description: Specifies a client signature when a call to the InitializeSecurityContext (Schannel) function cannot access the private key for a client certificate (in this case, the function returns SEC_I_SIGNATURE_NEEDED).
helpviewer_keywords: ["*PSCHANNEL_CLIENT_SIGNATURE","PSCHANNEL_CLIENT_SIGNATURE","PSCHANNEL_CLIENT_SIGNATURE structure pointer [Security]","SCHANNEL_CLIENT_SIGNATURE","SCHANNEL_CLIENT_SIGNATURE structure [Security]","schannel/PSCHANNEL_CLIENT_SIGNATURE","schannel/SCHANNEL_CLIENT_SIGNATURE","security.schannel_client_signature"]
old-location: security\schannel_client_signature.htm
tech.root: security
ms.assetid: 2549a287-bee3-457b-86e3-3330bf23169a
ms.date: 12/05/2018
ms.keywords: '*PSCHANNEL_CLIENT_SIGNATURE, PSCHANNEL_CLIENT_SIGNATURE, PSCHANNEL_CLIENT_SIGNATURE structure pointer [Security], SCHANNEL_CLIENT_SIGNATURE, SCHANNEL_CLIENT_SIGNATURE structure [Security], schannel/PSCHANNEL_CLIENT_SIGNATURE, schannel/SCHANNEL_CLIENT_SIGNATURE, security.schannel_client_signature'
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SCHANNEL_CLIENT_SIGNATURE, *PSCHANNEL_CLIENT_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_CLIENT_SIGNATURE
 - schannel/_SCHANNEL_CLIENT_SIGNATURE
 - PSCHANNEL_CLIENT_SIGNATURE
 - schannel/PSCHANNEL_CLIENT_SIGNATURE
 - SCHANNEL_CLIENT_SIGNATURE
 - schannel/SCHANNEL_CLIENT_SIGNATURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SCHANNEL_CLIENT_SIGNATURE
---

# SCHANNEL_CLIENT_SIGNATURE structure


## -description

Specifies a client signature when a call to the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function cannot access the <a href="/windows/desktop/SecGloss/p-gly">private key</a> for a client certificate (in this case, the function returns <b>SEC_I_SIGNATURE_NEEDED</b>).

## -struct-fields

### -field cbLength

The size, in bytes, of this structure.

### -field aiHash

The ID of the algorithm used to compute the <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the certificate.

### -field cbHash

The size, in bytes, of the <b>HashValue</b> array.

### -field HashValue

An array of byte values that specify the hash of the certificate.

### -field CertThumbprint

An array of byte values that specify the certificate thumbprint.

## -remarks

Add a client signature to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.