---
UID: NF:wincrypt.CertFindSubjectInSortedCTL
title: CertFindSubjectInSortedCTL function (wincrypt.h)
description: The CertFindSubjectInSortedCTL function attempts to find the specified subject in a sorted certificate trust list (CTL).
helpviewer_keywords: ["CertFindSubjectInSortedCTL","CertFindSubjectInSortedCTL function [Security]","_crypto2_certfindsubjectinsortedctl","security.certfindsubjectinsortedctl","wincrypt/CertFindSubjectInSortedCTL"]
old-location: security\certfindsubjectinsortedctl.htm
tech.root: security
ms.assetid: 027e89e6-3de0-440d-be70-2281778f9a1e
ms.date: 12/05/2018
ms.keywords: CertFindSubjectInSortedCTL, CertFindSubjectInSortedCTL function [Security], _crypto2_certfindsubjectinsortedctl, security.certfindsubjectinsortedctl, wincrypt/CertFindSubjectInSortedCTL
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertFindSubjectInSortedCTL
 - wincrypt/CertFindSubjectInSortedCTL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFindSubjectInSortedCTL
---

# CertFindSubjectInSortedCTL function


## -description

The <b>CertFindSubjectInSortedCTL</b> function attempts to find the specified subject in a sorted <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL). A subject can be identified either by the certificate's whole context or by any unique identifier of the certificate's subject, such as the SHA1 <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the certificate's issuer and serial number.

## -parameters

### -param pSubjectIdentifier [in]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure uniquely identifying the subject. The information in this structure can be a <a href="/windows/desktop/SecGloss/h-gly">hash</a> or any unique byte sequence.

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure to be searched.

### -param dwFlags [in]

Reserved for future use and must be <b>NULL</b>.

### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.

### -param pEncodedAttributes [out]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure containing a byte count and a pointer to the subject's encoded attributes.

## -returns

If the function succeeds and the subject identifier exists in the CTL, the return value is <b>TRUE</b>.

If the function fails and does not locate a matching subject identifier, the return value is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsubjectinsortedctl">CertEnumSubjectInSortedCTL</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate and Certificate Store Maintenance Functions</a>