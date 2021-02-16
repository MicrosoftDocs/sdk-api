---
UID: NS:wincrypt._CERT_RDN
title: CERT_RDN (wincrypt.h)
description: The CERT_RDN structure contains a relative distinguished name (RDN) consisting of an array of CERT_RDN_ATTR structures.
helpviewer_keywords: ["*PCERT_RDN","CERT_RDN","CERT_RDN structure [Security]","PCERT_RDN","PCERT_RDN structure pointer [Security]","_crypto2_cert_rdn","security.cert_rdn","wincrypt/CERT_RDN","wincrypt/PCERT_RDN"]
old-location: security\cert_rdn.htm
tech.root: security
ms.assetid: e84254b9-e9a7-4689-a12f-2772282c5433
ms.date: 12/05/2018
ms.keywords: '*PCERT_RDN, CERT_RDN, CERT_RDN structure [Security], PCERT_RDN, PCERT_RDN structure pointer [Security], _crypto2_cert_rdn, security.cert_rdn, wincrypt/CERT_RDN, wincrypt/PCERT_RDN'
req.header: wincrypt.h
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
req.typenames: CERT_RDN, *PCERT_RDN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_RDN
 - wincrypt/_CERT_RDN
 - PCERT_RDN
 - wincrypt/PCERT_RDN
 - CERT_RDN
 - wincrypt/CERT_RDN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_RDN
---

# CERT_RDN structure


## -description

The <b>CERT_RDN</b> structure contains a <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN) consisting of an array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structures.

## -struct-fields

### -field cRDNAttr

Number of elements in the <b>rgRDNAttr</b> array.

### -field rgRDNAttr

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_name_info">CERT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certisrdnattrsincertificatename">CertIsRDNAttrsInCertificateName</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>