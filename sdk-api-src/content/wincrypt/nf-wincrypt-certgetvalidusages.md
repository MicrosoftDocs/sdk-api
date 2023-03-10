---
UID: NF:wincrypt.CertGetValidUsages
title: CertGetValidUsages function (wincrypt.h)
description: Returns an array of usages that consist of the intersection of the valid usages for all certificates in an array of certificates.
helpviewer_keywords: ["CertGetValidUsages","CertGetValidUsages function [Security]","_crypto2_certgetvalidusages","security.certgetvalidusages","wincrypt/CertGetValidUsages"]
old-location: security\certgetvalidusages.htm
tech.root: security
ms.assetid: 1504f166-2fa9-4041-9d72-b150cd8baa8a
ms.date: 12/05/2018
ms.keywords: CertGetValidUsages, CertGetValidUsages function [Security], _crypto2_certgetvalidusages, security.certgetvalidusages, wincrypt/CertGetValidUsages
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertGetValidUsages
 - wincrypt/CertGetValidUsages
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
 - CertGetValidUsages
---

# CertGetValidUsages function


## -description

The <b>CertGetValidUsages</b> function returns an array of usages that consist of the intersection of the valid usages for all certificates in an array of certificates.

## -parameters

### -param cCerts [in]

The number of certificates in the array to be checked.

### -param rghCerts [in]

An array of certificates to be checked for valid usage.

### -param cNumOIDs [out]

The number of valid usages found as the intersection of the valid usages of all certificates in the array. If all of the certificates are valid for all usages, <i>cNumOIDs</i> is set to negative one (–1).

### -param rghOIDs [out]

An array of the <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) of the valid usages that are shared by all of the certificates in the <i>rghCerts</i> array. This parameter can be <b>NULL</b> to set the size of this structure for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbOIDs [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>rghOIDs</i> array and the strings pointed to. When the function returns, the <b>DWORD</b> value contains the number of bytes needed for the array.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.