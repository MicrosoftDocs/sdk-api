---
UID: NS:schannel._SecPkgContext_IssuerListInfoEx
title: SecPkgContext_IssuerListInfoEx (schannel.h)
description: The SecPkgContext_IssuerListInfoEx structure holds a list of trusted certification authorities (CAs).
helpviewer_keywords: ["*PSecPkgContext_IssuerListInfoEx","PSecPkgContext_IssuerListInfoEx","PSecPkgContext_IssuerListInfoEx structure pointer [Security]","SecPkgContext_IssuerListInfoEx","SecPkgContext_IssuerListInfoEx structure [Security]","_ssp_secpkgcontext_issuerlistinfoex","schannel/PSecPkgContext_IssuerListInfoEx","schannel/SecPkgContext_IssuerListInfoEx","security.secpkgcontext_issuerlistinfoex"]
old-location: security\secpkgcontext_issuerlistinfoex.htm
tech.root: security
ms.assetid: cf1ccd40-36bf-4597-b34f-d26cef63d800
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_IssuerListInfoEx, PSecPkgContext_IssuerListInfoEx, PSecPkgContext_IssuerListInfoEx structure pointer [Security], SecPkgContext_IssuerListInfoEx, SecPkgContext_IssuerListInfoEx structure [Security], _ssp_secpkgcontext_issuerlistinfoex, schannel/PSecPkgContext_IssuerListInfoEx, schannel/SecPkgContext_IssuerListInfoEx, security.secpkgcontext_issuerlistinfoex'
req.header: schannel.h
req.include-header: Schnlsp.h
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
req.typenames: SecPkgContext_IssuerListInfoEx, *PSecPkgContext_IssuerListInfoEx
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_IssuerListInfoEx
 - schannel/_SecPkgContext_IssuerListInfoEx
 - PSecPkgContext_IssuerListInfoEx
 - schannel/PSecPkgContext_IssuerListInfoEx
 - SecPkgContext_IssuerListInfoEx
 - schannel/SecPkgContext_IssuerListInfoEx
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
 - SecPkgContext_IssuerListInfoEx
---

# SecPkgContext_IssuerListInfoEx structure


## -description

The <b>SecPkgContext_IssuerListInfoEx</b> structure holds a list of trusted <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> (CAs). This structure is used by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security package</a> <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function.

This attribute is supported only by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

This attribute is available only to client applications and can be queried only after a call to the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function returns the value <b>SEC_E_INCOMPLETE_CREDENTIALS</b>.

## -struct-fields

### -field aIssuers

A pointer to 
an array of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structures that contains a list of the names of CAs that the server trusts.

When you have finished using the data in this array, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

### -field cIssuers

The number of names in <b>aIssuers</b>.