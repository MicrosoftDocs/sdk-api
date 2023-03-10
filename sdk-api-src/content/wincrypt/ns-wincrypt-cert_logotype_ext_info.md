---
UID: NS:wincrypt._CERT_LOGOTYPE_EXT_INFO
title: CERT_LOGOTYPE_EXT_INFO (wincrypt.h)
description: Contains a set of logotype information.
helpviewer_keywords: ["*PCERT_LOGOTYPE_EXT_INFO","CERT_LOGOTYPE_EXT_INFO","CERT_LOGOTYPE_EXT_INFO structure [Security]","PCERT_LOGOTYPE_EXT_INFO","PCERT_LOGOTYPE_EXT_INFO structure pointer [Security]","security.cert_logotype_ext_info","wincrypt/CERT_LOGOTYPE_EXT_INFO","wincrypt/PCERT_LOGOTYPE_EXT_INFO"]
old-location: security\cert_logotype_ext_info.htm
tech.root: security
ms.assetid: 5013241b-439e-4aea-9161-699ee69c65c9
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_EXT_INFO, CERT_LOGOTYPE_EXT_INFO, CERT_LOGOTYPE_EXT_INFO structure [Security], PCERT_LOGOTYPE_EXT_INFO, PCERT_LOGOTYPE_EXT_INFO structure pointer [Security], security.cert_logotype_ext_info, wincrypt/CERT_LOGOTYPE_EXT_INFO, wincrypt/PCERT_LOGOTYPE_EXT_INFO'
req.header: wincrypt.h
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
req.typenames: CERT_LOGOTYPE_EXT_INFO, *PCERT_LOGOTYPE_EXT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_EXT_INFO
 - wincrypt/_CERT_LOGOTYPE_EXT_INFO
 - PCERT_LOGOTYPE_EXT_INFO
 - wincrypt/PCERT_LOGOTYPE_EXT_INFO
 - CERT_LOGOTYPE_EXT_INFO
 - wincrypt/CERT_LOGOTYPE_EXT_INFO
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
 - CERT_LOGOTYPE_EXT_INFO
---

# CERT_LOGOTYPE_EXT_INFO structure


## -description

The <b>CERT_LOGOTYPE_EXT_INFO</b> structure contains a set of logotype information.

## -struct-fields

### -field cCommunityLogo

The number of elements in the <b>rgCommunityLogo</b> array.

### -field rgCommunityLogo

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_info">CERT_LOGOTYPE_INFO</a> structures that contain the community logotypes. The <b>cCommunityLogo</b>  member contains the number of elements in this array.

### -field pIssuerLogo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_info">CERT_LOGOTYPE_INFO</a> structure that contains the issuer logotype. This member is optional and may be <b>NULL</b>.

### -field pSubjectLogo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_info">CERT_LOGOTYPE_INFO</a> structure that contains the subject logotype. This member is optional and may be <b>NULL</b>.

### -field cOtherLogo

The number of elements in the <b>rgOtherLogo</b> array.

### -field rgOtherLogo

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_other_logotype_info">CERT_OTHER_LOGOTYPE_INFO</a> structures that contain any other logotypes. The <b>cOtherLogo</b>  member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a>