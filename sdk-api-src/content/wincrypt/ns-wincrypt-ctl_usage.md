---
UID: NS:wincrypt._CTL_USAGE
title: CTL_USAGE (wincrypt.h)
description: Contains an array of object identifiers (OIDs) for Certificate Trust List (CTL) extensions.
helpviewer_keywords: ["*PCERT_ENHKEY_USAGE","*PCTL_USAGE","CERT_ENHKEY_USAGE","CERT_ENHKEY_USAGE structure [Security]","CTL_USAGE","CTL_USAGE structure [Security]","PCERT_ENHKEY_USAGE","PCERT_ENHKEY_USAGE structure pointer [Security]","PCTL_USAGE","PCTL_USAGE structure pointer [Security]","_crypto2_ctl_usage","security.ctl_usage","wincrypt/CERT_ENHKEY_USAGE","wincrypt/CTL_USAGE","wincrypt/PCERT_ENHKEY_USAGE","wincrypt/PCTL_USAGE"]
old-location: security\ctl_usage.htm
tech.root: security
ms.assetid: 70ee138a-df94-4fc4-9de5-0d8b7704b890
ms.date: 12/05/2018
ms.keywords: '*PCERT_ENHKEY_USAGE, *PCTL_USAGE, CERT_ENHKEY_USAGE, CERT_ENHKEY_USAGE structure [Security], CTL_USAGE, CTL_USAGE structure [Security], PCERT_ENHKEY_USAGE, PCERT_ENHKEY_USAGE structure pointer [Security], PCTL_USAGE, PCTL_USAGE structure pointer [Security], _crypto2_ctl_usage, security.ctl_usage, wincrypt/CERT_ENHKEY_USAGE, wincrypt/CTL_USAGE, wincrypt/PCERT_ENHKEY_USAGE, wincrypt/PCTL_USAGE'
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
req.typenames: CTL_USAGE, *PCTL_USAGE, CERT_ENHKEY_USAGE, *PCERT_ENHKEY_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_USAGE
 - wincrypt/_CTL_USAGE
 - PCTL_USAGE
 - wincrypt/PCTL_USAGE
 - CTL_USAGE
 - wincrypt/CTL_USAGE
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
 - CTL_USAGE
---

# CTL_USAGE structure


## -description

The <b>CTL_USAGE</b> structure contains an array of <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) for <a href="/windows/desktop/SecGloss/c-gly">Certificate Trust List</a> (CTL) extensions. <b>CTL_USAGE</b> structures are used in functions that search for CTLs for specific uses.

## -struct-fields

### -field cUsageIdentifier

Number of elements in the <b>rgpszUsageIdentifier</b> member array.

### -field rgpszUsageIdentifier

Array of object identifiers (OIDs) of CTL extensions.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>