---
UID: NF:wincrypt.CryptInstallOIDFunctionAddress
title: CryptInstallOIDFunctionAddress function (wincrypt.h)
description: The CryptInstallOIDFunctionAddress function installs a set of callable object identifier (OID) function addresses.
helpviewer_keywords: ["CryptInstallOIDFunctionAddress","CryptInstallOIDFunctionAddress function [Security]","_crypto2_cryptinstalloidfunctionaddress","security.cryptinstalloidfunctionaddress","wincrypt/CryptInstallOIDFunctionAddress"]
old-location: security\cryptinstalloidfunctionaddress.htm
tech.root: security
ms.assetid: 934e8278-0e0b-4402-a2b6-ff1e913d54c9
ms.date: 12/05/2018
ms.keywords: CryptInstallOIDFunctionAddress, CryptInstallOIDFunctionAddress function [Security], _crypto2_cryptinstalloidfunctionaddress, security.cryptinstalloidfunctionaddress, wincrypt/CryptInstallOIDFunctionAddress
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
 - CryptInstallOIDFunctionAddress
 - wincrypt/CryptInstallOIDFunctionAddress
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
 - CryptInstallOIDFunctionAddress
---

# CryptInstallOIDFunctionAddress function


## -description

The <b>CryptInstallOIDFunctionAddress</b> function installs a set of callable <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) function addresses.

## -parameters

### -param hModule [in]

This parameter is updated with the <i>hModule</i> parameter passed to <b>DllMain</b> to prevent the DLL that contains the function addresses from being unloaded by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a> or
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress">CryptFreeOIDFunctionAddress</a>. This would be the case when the DLL has also registered OID functions through 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidfunction">CryptRegisterOIDFunction</a>.

### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

### -param pszFuncName [in]

Name of the function set being installed.

### -param cFuncEntry [in]

Number of array elements in <i>rgFuncEntry</i>[].

### -param rgFuncEntry [in]

Array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_func_entry">CRYPT_OID_FUNC_ENTRY</a> structures, each containing an OID and the starting address of its correlated routine. 
					

Default functions are installed by setting the <b>pszOID</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_func_entry">CRYPT_OID_FUNC_ENTRY</a> structure for their array element to CRYPT_DEFAULT_OID.

### -param dwFlags [in]

By default, a new function set is installed at the end of the list of function sets. Setting the CRYPT_INSTALL_OID_FUNC_BEFORE_FLAG flag installs the function set at the beginning of the list.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_func_entry">CRYPT_OID_FUNC_ENTRY</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>