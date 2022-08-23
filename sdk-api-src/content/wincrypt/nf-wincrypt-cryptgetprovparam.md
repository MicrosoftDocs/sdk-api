---
UID: NF:wincrypt.CryptGetProvParam
title: CryptGetProvParam function (wincrypt.h)
description: Retrieves parameters that govern the operations of a cryptographic service provider (CSP).
helpviewer_keywords: ["CRYPT_FASTSGC","CRYPT_FIRST","CRYPT_NEXT","CRYPT_SGC","CRYPT_SGC_ENUM","CryptGetProvParam","CryptGetProvParam function [Security]","DACL_SECURITY_INFORMATION","GROUP_SECURITY_INFORMATION","OWNER_SECURITY_INFORMATION","PP_ADMIN_PIN","PP_APPLI_CERT","PP_CERTCHAIN","PP_CHANGE_PASSWORD","PP_CONTAINER","PP_CRYPT_COUNT_KEY_USE","PP_ENUMALGS","PP_ENUMALGS_EX","PP_ENUMCONTAINERS","PP_ENUMELECTROOTS","PP_ENUMEX_SIGNING_PROT","PP_ENUMMANDROOTS","PP_IMPTYPE","PP_KEYEXCHANGE_PIN","PP_KEYSET_SEC_DESCR","PP_KEYSET_TYPE","PP_KEYSPEC","PP_KEYSTORAGE","PP_KEYX_KEYSIZE_INC","PP_KEY_TYPE_SUBTYPE","PP_NAME","PP_PROVTYPE","PP_ROOT_CERTSTORE","PP_SESSION_KEYSIZE","PP_SGC_INFO","PP_SIGNATURE_PIN","PP_SIG_KEYSIZE_INC","PP_SMARTCARD_GUID","PP_SMARTCARD_READER","PP_SYM_KEYSIZE","PP_UI_PROMPT","PP_UNIQUE_CONTAINER","PP_USER_CERTSTORE","PP_USE_HARDWARE_RNG","PP_VERSION","SACL_SECURITY_INFORMATION","_crypto2_cryptgetprovparam","security.cryptgetprovparam","wincrypt/CryptGetProvParam"]
old-location: security\cryptgetprovparam.htm
tech.root: security
ms.assetid: c0b7c1c8-aa42-4d40-a7f7-99c0821c8977
ms.date: 12/05/2018
ms.keywords: CRYPT_FASTSGC, CRYPT_FIRST, CRYPT_NEXT, CRYPT_SGC, CRYPT_SGC_ENUM, CryptGetProvParam, CryptGetProvParam function [Security], DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, OWNER_SECURITY_INFORMATION, PP_ADMIN_PIN, PP_APPLI_CERT, PP_CERTCHAIN, PP_CHANGE_PASSWORD, PP_CONTAINER, PP_CRYPT_COUNT_KEY_USE, PP_ENUMALGS, PP_ENUMALGS_EX, PP_ENUMCONTAINERS, PP_ENUMELECTROOTS, PP_ENUMEX_SIGNING_PROT, PP_ENUMMANDROOTS, PP_IMPTYPE, PP_KEYEXCHANGE_PIN, PP_KEYSET_SEC_DESCR, PP_KEYSET_TYPE, PP_KEYSPEC, PP_KEYSTORAGE, PP_KEYX_KEYSIZE_INC, PP_KEY_TYPE_SUBTYPE, PP_NAME, PP_PROVTYPE, PP_ROOT_CERTSTORE, PP_SESSION_KEYSIZE, PP_SGC_INFO, PP_SIGNATURE_PIN, PP_SIG_KEYSIZE_INC, PP_SMARTCARD_GUID, PP_SMARTCARD_READER, PP_SYM_KEYSIZE, PP_UI_PROMPT, PP_UNIQUE_CONTAINER, PP_USER_CERTSTORE, PP_USE_HARDWARE_RNG, PP_VERSION, SACL_SECURITY_INFORMATION, _crypto2_cryptgetprovparam, security.cryptgetprovparam, wincrypt/CryptGetProvParam
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetProvParam
 - wincrypt/CryptGetProvParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptGetProvParam
---

# CryptGetProvParam function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGetProvParam</b> function retrieves parameters that govern the operations of a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -parameters

### -param hProv [in]

 A handle of the CSP target of the query. This handle must have been created by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function.

### -param dwParam [in]

The nature of the query. The following queries are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PP_ADMIN_PIN"></a><a id="pp_admin_pin"></a><dl>
<dt><b>PP_ADMIN_PIN</b></dt>
<dt>31 (0x1F)</dt>
</dl>
</td>
<td width="60%">
Returns the administrator personal identification number (PIN) in the <i>pbData</i> parameter as a <b>LPSTR</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_APPLI_CERT"></a><a id="pp_appli_cert"></a><dl>
<dt><b>PP_APPLI_CERT</b></dt>
<dt>18 (0x12)</dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_CHANGE_PASSWORD"></a><a id="pp_change_password"></a><dl>
<dt><b>PP_CHANGE_PASSWORD</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_CERTCHAIN"></a><a id="pp_certchain"></a><dl>
<dt><b>PP_CERTCHAIN</b></dt>
<dt>9 (0x9)</dt>
</dl>
</td>
<td width="60%">
Returns the certificate chain associated with the <i>hProv</i> handle. The returned certificate chain is <b>X509_ASN_ENCODING</b> encoded.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_CONTAINER"></a><a id="pp_container"></a><dl>
<dt><b>PP_CONTAINER</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">
The name of the current <a href="/windows/desktop/SecGloss/k-gly">key container</a> as a <b>null</b>-terminated <b>CHAR</b> string. This string is exactly the same as the one passed in the <i>pszContainer</i> parameter of the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function to specify the key container to use. The <i>pszContainer</i> parameter can be read to determine the name of the default key container.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_CRYPT_COUNT_KEY_USE"></a><a id="pp_crypt_count_key_use"></a><dl>
<dt><b>PP_CRYPT_COUNT_KEY_USE</b></dt>
<dt>41 (0x29)</dt>
</dl>
</td>
<td width="60%">
Not implemented by Microsoft CSPs. This behavior may be implemented by other CSPs.

<b>Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMALGS"></a><a id="pp_enumalgs"></a><dl>
<dt><b>PP_ENUMALGS</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
A 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-prov_enumalgs">PROV_ENUMALGS</a> structure that contains information about one algorithm supported by the CSP being queried.

The first time this value is read, the <i>dwFlags</i> parameter must contain the <b>CRYPT_FIRST</b> flag. Doing so causes this function to retrieve the first element in the enumeration. The subsequent elements can then be retrieved by setting the <b>CRYPT_NEXT</b> flag in the <i>dwFlags</i> parameter. When this function fails with the <b>ERROR_NO_MORE_ITEMS</b> error code, the end of the enumeration has been reached.

This function is not thread safe, and all of the available algorithms might not be enumerated if this function is used in a multithreaded context.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMALGS_EX"></a><a id="pp_enumalgs_ex"></a><dl>
<dt><b>PP_ENUMALGS_EX</b></dt>
<dt>22 (0x16)</dt>
</dl>
</td>
<td width="60%">
A 
								<a href="/windows/desktop/api/wincrypt/ns-wincrypt-prov_enumalgs_ex">PROV_ENUMALGS_EX</a> structure that contains information about one algorithm supported by the CSP being queried. The structure returned contains more information about the algorithm than the structure returned for PP_ENUMALGS.

The first time this value is read, the <i>dwFlags</i> parameter must contain the <b>CRYPT_FIRST</b> flag. Doing so causes this function to retrieve the first element in the enumeration. The subsequent elements can then be retrieved by setting the <b>CRYPT_NEXT</b> flag in the <i>dwFlags</i> parameter. When this function fails with the <b>ERROR_NO_MORE_ITEMS</b> error code, the end of the enumeration has been reached.

This function is not thread safe and all of the available algorithms might not be enumerated if this function is used in a multithreaded context.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMCONTAINERS"></a><a id="pp_enumcontainers"></a><dl>
<dt><b>PP_ENUMCONTAINERS</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The name of one of the key containers maintained by the CSP in the form of a <b>null</b>-terminated <b>CHAR</b> string. 

The first time this value is read, the <i>dwFlags</i> parameter must contain the <b>CRYPT_FIRST</b> flag. Doing so causes this function to retrieve the first element in the enumeration. The subsequent elements can then be retrieved by setting the <b>CRYPT_NEXT</b> flag in the <i>dwFlags</i> parameter. When this function fails with the <b>ERROR_NO_MORE_ITEMS</b> error code, the end of the enumeration has been reached.

To enumerate key containers associated with a computer, first call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> using the <b>CRYPT_MACHINE_KEYSET</b> flag, and then use the handle returned from <b>CryptAcquireContext</b> as the <i>hProv</i> parameter in the call to <b>CryptGetProvParam</b>.

This function is not thread safe and all of the available algorithms might not be enumerated if this function is used in a multithreaded context.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMELECTROOTS"></a><a id="pp_enumelectroots"></a><dl>
<dt><b>PP_ENUMELECTROOTS</b></dt>
<dt>26 (0x1A)</dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMEX_SIGNING_PROT"></a><a id="pp_enumex_signing_prot"></a><dl>
<dt><b>PP_ENUMEX_SIGNING_PROT</b></dt>
<dt>40 (0x28)</dt>
</dl>
</td>
<td width="60%">
Indicates that the current CSP supports the <b>dwProtocols</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-prov_enumalgs_ex">PROV_ENUMALGS_EX</a> structure. If this function succeeds, the CSP supports the <b>dwProtocols</b> member of the <b>PROV_ENUMALGS_EX</b> structure. If this function fails with an <b>NTE_BAD_TYPE</b> error code, the CSP does not support the <b>dwProtocols</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ENUMMANDROOTS"></a><a id="pp_enummandroots"></a><dl>
<dt><b>PP_ENUMMANDROOTS</b></dt>
<dt>25 (0x19)</dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_IMPTYPE"></a><a id="pp_imptype"></a><dl>
<dt><b>PP_IMPTYPE</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
A <b>DWORD</b> value that indicates how the CSP is implemented. For a table of possible values, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEY_TYPE_SUBTYPE"></a><a id="pp_key_type_subtype"></a><dl>
<dt><b>PP_KEY_TYPE_SUBTYPE</b></dt>
<dt>10 (0xA)</dt>
</dl>
</td>
<td width="60%">
This query is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYEXCHANGE_PIN"></a><a id="pp_keyexchange_pin"></a><dl>
<dt><b>PP_KEYEXCHANGE_PIN</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
Specifies that the key exchange PIN is contained in <i>pbData</i>. The PIN is represented as a <b>null</b>-terminated ASCII string.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYSET_SEC_DESCR"></a><a id="pp_keyset_sec_descr"></a><dl>
<dt><b>PP_KEYSET_SEC_DESCR</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Retrieves the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the key storage container. The <i>pbData</i> parameter is the address of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that receives the security descriptor for the key storage container. The security descriptor is returned in self-relative format.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYSET_TYPE"></a><a id="pp_keyset_type"></a><dl>
<dt><b>PP_KEYSET_TYPE</b></dt>
<dt>27 (0x1B)</dt>
</dl>
</td>
<td width="60%">
Determines whether the <i>hProv</i> parameter is a computer key set. The <i>pbData</i> parameter must be a <b>DWORD</b>; the <b>DWORD</b> will be set to the CRYPT_MACHINE_KEYSET flag if that flag was passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYSPEC"></a><a id="pp_keyspec"></a><dl>
<dt><b>PP_KEYSPEC</b></dt>
<dt>39 (0x27)</dt>
</dl>
</td>
<td width="60%">
Returns information about the key specifier values that the CSP supports. Key specifier values are joined in a logical <b>OR</b> and returned in the <i>pbData</i> parameter of the call as a <b>DWORD</b>. For example, the Microsoft Base Cryptographic Provider version 1.0 returns a <b>DWORD</b> value of AT_SIGNATURE | AT_KEYEXCHANGE.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYSTORAGE"></a><a id="pp_keystorage"></a><dl>
<dt><b>PP_KEYSTORAGE</b></dt>
<dt>17 (0x11)</dt>
</dl>
</td>
<td width="60%">
Returns a <b>DWORD</b> value of CRYPT_SEC_DESCR.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYX_KEYSIZE_INC"></a><a id="pp_keyx_keysize_inc"></a><dl>
<dt><b>PP_KEYX_KEYSIZE_INC</b></dt>
<dt>35 (0x23)</dt>
</dl>
</td>
<td width="60%">
The number of bits for the increment length of AT_KEYEXCHANGE. This information is used with information returned in the PP_ENUMALGS_EX value. With the information returned when using PP_ENUMALGS_EX and PP_KEYX_KEYSIZE_INC, the valid key lengths for AT_KEYEXCHANGE can be determined. These key lengths can then be used with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>. For example if a CSP enumerates <a href="/windows/desktop/SecGloss/c-gly">CALG_RSA_KEYX</a> (AT_KEYEXCHANGE) with a minimum key length of 512 bits and a maximum of 1024 bits, and returns the increment length as 64 bits, then valid key lengths are 512, 576, 640,… 1024.
							

</td>
</tr>
<tr>
<td width="40%"><a id="PP_NAME"></a><a id="pp_name"></a><dl>
<dt><b>PP_NAME</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The name of the CSP in the form of a <b>null</b>-terminated <b>CHAR</b> string. This string is identical to the one passed in the <i>pszProvider</i> parameter of the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function to specify that the current CSP be used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_PROVTYPE"></a><a id="pp_provtype"></a><dl>
<dt><b>PP_PROVTYPE</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
A <b>DWORD</b> value that indicates the provider type of the CSP.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ROOT_CERTSTORE"></a><a id="pp_root_certstore"></a><dl>
<dt><b>PP_ROOT_CERTSTORE</b></dt>
<dt>46 (0x2E)</dt>
</dl>
</td>
<td width="60%">
Obtains the root certificate store for the smart card. This certificate store contains all of the root certificates that are stored on the smart card.

The <i>pbData</i> parameter is the address of an <b>HCERTSTORE</b> variable that receives the handle of the certificate store. When this handle is no longer needed, the caller must close it by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SESSION_KEYSIZE"></a><a id="pp_session_keysize"></a><dl>
<dt><b>PP_SESSION_KEYSIZE</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">
The size, in bits, of the session key.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SGC_INFO"></a><a id="pp_sgc_info"></a><dl>
<dt><b>PP_SGC_INFO</b></dt>
<dt>37 (0x25)</dt>
</dl>
</td>
<td width="60%">
Used with <a href="/windows/desktop/SecGloss/s-gly">server gated cryptography</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SIG_KEYSIZE_INC"></a><a id="pp_sig_keysize_inc"></a><dl>
<dt><b>PP_SIG_KEYSIZE_INC</b></dt>
<dt>34 (0x22)</dt>
</dl>
</td>
<td width="60%">
The number of bits for the increment length of AT_SIGNATURE. This information is used with information returned in the PP_ENUMALGS_EX value. With the information returned when using PP_ENUMALGS_EX and PP_SIG_KEYSIZE_INC, the valid <a href="/windows/desktop/SecGloss/k-gly">key lengths</a> for AT_SIGNATURE can be determined. These key lengths can then be used with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>.

For example, if a CSP enumerates <a href="/windows/desktop/SecGloss/c-gly">CALG_RSA_SIGN</a> (AT_SIGNATURE) with a minimum <a href="/windows/desktop/SecGloss/k-gly">key length</a> of 512 bits and a maximum of 1024 bits, and returns the increment length as 64 bits, then valid key lengths are 512, 576, 640,… 1024.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SIGNATURE_PIN"></a><a id="pp_signature_pin"></a><dl>
<dt><b>PP_SIGNATURE_PIN</b></dt>
<dt>33 (0x21)</dt>
</dl>
</td>
<td width="60%">
Specifies that the key signature PIN is contained in <i>pbData</i>. The PIN is represented as a <b>null</b>-terminated ASCII string.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SMARTCARD_GUID"></a><a id="pp_smartcard_guid"></a><dl>
<dt><b>PP_SMARTCARD_GUID</b></dt>
<dt>45 (0x2D)</dt>
</dl>
</td>
<td width="60%">
Obtains the identifier of the smart card. The <i>pbData</i> parameter is the address of a <b>GUID</b> structure that receives the identifier of the smart card.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SMARTCARD_READER"></a><a id="pp_smartcard_reader"></a><dl>
<dt><b>PP_SMARTCARD_READER</b></dt>
<dt>43 (0x2B)</dt>
</dl>
</td>
<td width="60%">
Obtains the name of the smart card reader. The <i>pbData</i> parameter is the address of an ANSI character array that receives a <b>null</b>-terminated ANSI string that contains the name of the smart card reader. The size of this buffer, contained in the variable pointed to by the <i>pdwDataLen</i> parameter, must include the <b>NULL</b> terminator.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SYM_KEYSIZE"></a><a id="pp_sym_keysize"></a><dl>
<dt><b>PP_SYM_KEYSIZE</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">
The size of the symmetric key.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_UI_PROMPT"></a><a id="pp_ui_prompt"></a><dl>
<dt><b>PP_UI_PROMPT</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">
This query  is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_UNIQUE_CONTAINER"></a><a id="pp_unique_container"></a><dl>
<dt><b>PP_UNIQUE_CONTAINER</b></dt>
<dt>36 (0x24)</dt>
</dl>
</td>
<td width="60%">
The unique container name of the current key container in the form of a <b>null</b>-terminated <b>CHAR</b> string. For many CSPs, this name is the same name returned when the PP_CONTAINER value is used. The 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function must work with this container name.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_USE_HARDWARE_RNG"></a><a id="pp_use_hardware_rng"></a><dl>
<dt><b>PP_USE_HARDWARE_RNG</b></dt>
<dt>38 (0x26)</dt>
</dl>
</td>
<td width="60%">
Indicates whether a hardware random number generator (RNG) is supported. When <b>PP_USE_HARDWARE_RNG</b> is specified, the function succeeds and returns <b>TRUE</b> if a hardware RNG is supported. The function fails and returns <b>FALSE</b> if a hardware RNG is not supported. If a RNG is supported, <b>PP_USE_HARDWARE_RNG</b> can be set in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a> to indicate that the CSP must exclusively use the hardware RNG for this provider context. When <b>PP_USE_HARDWARE_RNG</b> is used, the <i>pbData</i> parameter must be <b>NULL</b> and <i>dwFlags</i> must be zero.

None of the Microsoft CSPs currently support using a hardware RNG.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_USER_CERTSTORE"></a><a id="pp_user_certstore"></a><dl>
<dt><b>PP_USER_CERTSTORE</b></dt>
<dt>42 (0x2A)</dt>
</dl>
</td>
<td width="60%">
Obtains the user certificate store for the smart card. This certificate store contains all of the user certificates that are stored on the smart card. The certificates in this store are encoded by using PKCS_7_ASN_ENCODING or X509_ASN_ENCODING encoding and should contain the <b>CERT_KEY_PROV_INFO_PROP_ID</b> property. 

The <i>pbData</i> parameter is the address of an <b>HCERTSTORE</b> variable that receives the handle of an in-memory certificate store. When this handle is no longer needed, the caller must close it by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_VERSION"></a><a id="pp_version"></a><dl>
<dt><b>PP_VERSION</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
The version number of the CSP. The least significant byte contains the minor version number and the next most significant byte the major version number. Version 2.0 is represented as 0x00000200. To maintain backward compatibility with earlier versions of the 
<a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft Base Cryptographic Provider</a> and the 
<a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a>, the provider names retain the "v1.0" designation in later versions.

</td>
</tr>
</table>

### -param pbData [out]

A pointer to a buffer to receive the data. The form of this data varies depending on the value of <i>dwParam</i>. When <i>dwParam</i> is set to PP_USE_HARDWARE_RNG, <i>pbData</i> must be set to <b>NULL</b>.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the buffer pointed to by the <i>pbData</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored or to be stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.

<p class="note">If PP_ENUMALGS, or PP_ENUMALGS_EX is set, the <i>pdwDataLen</i> parameter works somewhat differently. If <i>pbData</i> is <b>NULL</b> or the value pointed to by <i>pdwDataLen</i> is too small, the value returned in this parameter is the size of the largest item in the enumeration list instead of the size of the item currently being read.

<p class="note">If PP_ENUMCONTAINERS is set, the first call to the function returns the size of the maximum key-container allowed by the current provider. This is in contrast to other possible behaviors, like returning the length of the longest existing container, or the length of the current container. Subsequent enumerating calls will not change the <i>dwLen</i> parameter. For each enumerated container, the caller can determine the length of the <b>null</b>-terminated string programmatically, if desired. If one of the enumeration values is read and the <i>pbData</i> parameter is <b>NULL</b>, the CRYPT_FIRST flag must be specified for the size information to be correctly retrieved.

</div>
<div> </div>

### -param dwFlags [in]

If <i>dwParam</i> is <b>PP_KEYSET_SEC_DESCR</b>, the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> on the <a href="/windows/desktop/SecGloss/k-gly">key container</a> where the keys are stored is retrieved. For this case, <i>dwFlags</i> is used to pass in the <b>SECURITY_INFORMATION</b> bit flags that indicate the requested security information, as defined in the Platform SDK. <b>SECURITY_INFORMATION</b> bit flags can be combined with a bitwise-<b>OR</b> operation.
						
					


The following values are defined for use with <b>PP_KEYSET_SEC_DESCR</b>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OWNER_SECURITY_INFORMATION"></a><a id="owner_security_information"></a><dl>
<dt><b>OWNER_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Owner identifier of the object is being referenced.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Primary group identifier of the object is being referenced.

</td>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Discretionary ACL of the object is being referenced.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
System ACL of the object is being referenced.

</td>
</tr>
</table>
 


The following values are defined for use with <b>PP_ENUMALGS</b>, <b>PP_ENUMALGS_EX</b>, and <b>PP_ENUMCONTAINERS</b>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FIRST"></a><a id="crypt_first"></a><dl>
<dt><b>CRYPT_FIRST</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Retrieve the first element in the enumeration. This has the same effect as resetting the enumerator.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NEXT"></a><a id="crypt_next"></a><dl>
<dt><b>CRYPT_NEXT</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Retrieve the next element in the enumeration. When there are no more elements to retrieve, this function will fail and set the last error to <b>ERROR_NO_MORE_ITEMS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SGC_ENUM"></a><a id="crypt_sgc_enum"></a><dl>
<dt><b>CRYPT_SGC_ENUM</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Retrieve <a href="/windows/desktop/SecGloss/s-gly">server-gated cryptography</a> (SGC) enabled certificates. SGC enabled certificates are no longer supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SGC"></a><a id="crypt_sgc"></a><dl>
<dt><b>CRYPT_SGC</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FASTSGC"></a><a id="crypt_fastsgc"></a><dl>
<dt><b>CRYPT_FASTSGC</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by NTE are generated by the particular CSP being used. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbData</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pdwDataLen</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The end of the enumeration list has been reached. No valid data has been placed in the <i>pbData</i> buffer. This error code is returned only when <i>dwParam</i> equals PP_ENUMALGS or PP_ENUMCONTAINERS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter specifies a flag that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwParam</i> parameter specifies an unknown value number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP <a href="/windows/desktop/SecGloss/c-gly">context</a> specified by <i>hProv</i> is not valid.

</td>
</tr>
</table>

## -remarks

This function must not be used on a thread of a multithreaded program.

The following values are returned in <i>pbData</i> if <i>dwParam</i> is PP_IMPTYPE.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CRYPT_IMPL_HARDWARE<br/>
0x01
</td>
<td>Implementation is in hardware.</td>
</tr>
<tr>
<td>CRYPT_IMPL_SOFTWARE<br/>
0x02
</td>
<td>Implementation is in software.</td>
</tr>
<tr>
<td>CRYPT_IMPL_MIXED<br/>
0x03
</td>
<td>Implementation involves both hardware and software.</td>
</tr>
<tr>
<td>CRYPT_IMPL_UNKNOWN<br/>
0x04
</td>
<td>Implementation type is unknown.</td>
</tr>
<tr>
<td>CRYPT_IMPL_REMOVABLE<br/>
0x08
	
</td>
<td>Implementation is in removable media.</td>
</tr>
</table>
 



The <i>dwFlags</i> parameter is used to pass in the <b>SECURITY_INFORMATION</b> bit flags that indicate the requested security information. The pointer to the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> is returned in the <i>pbData</i> parameter and the length of the security descriptor is returned in the <i>pdwDataLen</i> parameter. Key-container security is handled with 
<a href="/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a> and 
<a href="/windows/desktop/api/winbase/nf-winbase-getfilesecuritya">GetFileSecurity</a>.


The class of an algorithm enumerated with <i>dwParam</i> set to PP_ENUMALGS or PP_ENUMALGS_EX can be determined. This might be done to display a list of encryption algorithms supported and to disregard the rest. The <b>GET_ALG_CLASS(</b><i>x</i><b>)</b> macro takes an algorithm identifier as an argument and returns a code indicating the general class of that algorithm. Possible return values include:

<ul>
<li>ALG_CLASS_DATA_ENCRYPT</li>
<li>ALG_CLASS_HASH</li>
<li>ALG_CLASS_KEY_EXCHANGE</li>
<li>ALG_CLASS_SIGNATURE</li>
</ul>


The following table lists the algorithms supported by the Microsoft Base Cryptographic Provider along with the class of each algorithm.<table>
<tr>
<th>Name</th>
<th>Identifier</th>
<th>Class</th>
</tr>
<tr>
<td>"MD2"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_MD2</a></td>
<td>ALG_CLASS_HASH</td>
</tr>
<tr>
<td>"MD5"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_MD5</a></td>
<td>ALG_CLASS_HASH</td>
</tr>
<tr>
<td>"SHA"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_SHA</a></td>
<td>ALG_CLASS_HASH</td>
</tr>
<tr>
<td>"MAC"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_MAC</a></td>
<td>ALG_CLASS_HASH</td>
</tr>
<tr>
<td>"RSA_SIGN"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_RSA_SIGN</a></td>
<td>ALG_CLASS_SIGNATURE</td>
</tr>
<tr>
<td>"RSA_KEYX"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_RSA_KEYX</a></td>
<td>ALG_CLASS_KEY_EXCHANGE</td>
</tr>
<tr>
<td>"RC2"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_RC2</a></td>
<td>ALG_CLASS_DATA_ENCRYPT</td>
</tr>
<tr>
<td>"RC4"</td>
<td><a href="/windows/desktop/SecGloss/c-gly">CALG_RC4</a></td>
<td>ALG_CLASS_DATA_ENCRYPT</td>
</tr>
</table>
 



Applications must not use an algorithm with an algorithm identifier that is not recognized. Using an unknown cryptographic algorithm can produce unpredictable results.


#### Examples

The following example shows finding the name of the CSP associated with a cryptographic service provider handle and the name of the key container associated with the handle. For the complete context for this example, see 
<a href="/windows/desktop/SecCrypto/example-c-program-using-cryptacquirecontext">Example C Program: Using CryptAcquireContext</a>. 

For another example that  uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-enumerating-csp-providers-and-provider-types">Example C Program: Enumerating CSP Providers and Provider Types</a>.


```cpp
//-----------------------------------------------------------------
//  Declare and initialize variables.

HCRYPTPROV hCryptProv;
BYTE       pbData[1000];       // 1000 will hold the longest 
                               // key container name.
DWORD cbData;

//-------------------------------------------------------------------
// An HCRYPTPROV must be acquired before using code like that in 
// "Example C Program Using CryptAcquireContext."

//-------------------------------------------------------------------
// Read the name of the default CSP.

cbData = 1000;
if(CryptGetProvParam(
    hCryptProv, 
    PP_NAME, 
    pbData, 
    &cbData, 
    0))
{
    printf("CryptGetProvParam succeeded.\n");
    printf("Provider name: %s\n", pbData);
}
else
{
    printf("Error reading CSP name. \n");
    exit(1);
}
//--------------------------------------------------------------------
// Read the name of the default key container.

cbData = 1000;
if(CryptGetProvParam(
    hCryptProv, 
    PP_CONTAINER, 
    pbData, 
    &cbData, 
    0))
{
    printf("CryptGetProvParam succeeded. \n");
    printf("Key Container name: %s\n", pbData);
}
else
{
    printf("Error reading key container name. \n");
    exit(1);
}
```

## -see-also

<a href="/windows/desktop/SecAuthZ/absolute-and-self-relative-security-descriptors">Absolute and Self-Relative Security Descriptors</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptderivekey">CryptDeriveKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>
