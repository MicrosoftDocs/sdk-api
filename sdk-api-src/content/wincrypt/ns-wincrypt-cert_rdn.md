---
UID: NS:wincrypt._CERT_RDN
title: CERT_RDN (wincrypt.h)
author: windows-sdk-content
description: The CERT_RDN structure contains a relative distinguished name (RDN) consisting of an array of CERT_RDN_ATTR structures.
old-location: security\cert_rdn.htm
tech.root: SecCrypto
ms.assetid: e84254b9-e9a7-4689-a12f-2772282c5433
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCERT_RDN, CERT_RDN, CERT_RDN structure [Security], PCERT_RDN, PCERT_RDN structure pointer [Security], _crypto2_cert_rdn, security.cert_rdn, wincrypt/CERT_RDN, wincrypt/PCERT_RDN'
ms.topic: struct
f1_keywords:
- wincrypt/CERT_RDN
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincrypt.h
api_name:
- CERT_RDN
targetos: Windows
req.typenames: CERT_RDN, *PCERT_RDN
req.redist: 
ms.custom: 19H1
---

# CERT_RDN structure


## -description


The <b>CERT_RDN</b> structure contains a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN) consisting of an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structures.


## -struct-fields




### -field cRDNAttr

Number of elements in the <b>rgRDNAttr</b> array.


### -field rgRDNAttr

Array of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structures.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_name_info">CERT_NAME_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certisrdnattrsincertificatename">CertIsRDNAttrsInCertificateName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>
 

 

