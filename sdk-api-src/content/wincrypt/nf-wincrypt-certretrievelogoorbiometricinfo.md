---
UID: NF:wincrypt.CertRetrieveLogoOrBiometricInfo
title: CertRetrieveLogoOrBiometricInfo function (wincrypt.h)
description: Performs a URL retrieval of logo or biometric information specified in either the szOID_LOGOTYPE_EXT or szOID_BIOMETRIC_EXT certificate extension.
helpviewer_keywords: ["CERT_RETRIEVE_BIOMETRIC_PICTURE_TYPE","CERT_RETRIEVE_BIOMETRIC_SIGNATURE_TYPE","CERT_RETRIEVE_COMMUNITY_LOGO","CERT_RETRIEVE_ISSUER_LOGO","CERT_RETRIEVE_SUBJECT_LOGO","CertRetrieveLogoOrBiometricInfo","CertRetrieveLogoOrBiometricInfo function [Security]","security.certretrievelogoorbiometricinfo","wincrypt/CertRetrieveLogoOrBiometricInfo"]
old-location: security\certretrievelogoorbiometricinfo.htm
tech.root: security
ms.assetid: 35813928-728e-40b7-b627-817d3094eeb1
ms.date: 12/05/2018
ms.keywords: CERT_RETRIEVE_BIOMETRIC_PICTURE_TYPE, CERT_RETRIEVE_BIOMETRIC_SIGNATURE_TYPE, CERT_RETRIEVE_COMMUNITY_LOGO, CERT_RETRIEVE_ISSUER_LOGO, CERT_RETRIEVE_SUBJECT_LOGO, CertRetrieveLogoOrBiometricInfo, CertRetrieveLogoOrBiometricInfo function [Security], security.certretrievelogoorbiometricinfo, wincrypt/CertRetrieveLogoOrBiometricInfo
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertRetrieveLogoOrBiometricInfo
 - wincrypt/CertRetrieveLogoOrBiometricInfo
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
 - CertRetrieveLogoOrBiometricInfo
---

# CertRetrieveLogoOrBiometricInfo function


## -description

The <b>CertRetrieveLogoOrBiometricInfo</b> function performs a URL retrieval of logo or biometric information specified in either the <b>szOID_LOGOTYPE_EXT</b> or <b>szOID_BIOMETRIC_EXT</b> certificate extension. The <b>szOID_BIOMETRIC_EXT</b> extension (IETF RFC 3739) supports the addition of a signature or a pictorial representation of the human holder of the certificate. The <b>szOID_LOGOTYPE_EXT</b> extension (IETF RFC 3709) supports the addition of organizational pictorial representations in certificates.

## -parameters

### -param pCertContext [in]

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate.

### -param lpszLogoOrBiometricType [in]

The address of a null-terminated ANSI string that contains an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) string that identifies the type of information to retrieve.


This parameter may also contain one of the following predefined values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_RETRIEVE_ISSUER_LOGO"></a><a id="cert_retrieve_issuer_logo"></a><dl>
<dt><b>CERT_RETRIEVE_ISSUER_LOGO</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the certificate issuer logotype.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RETRIEVE_SUBJECT_LOGO"></a><a id="cert_retrieve_subject_logo"></a><dl>
<dt><b>CERT_RETRIEVE_SUBJECT_LOGO</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the certificate subject logotype.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RETRIEVE_COMMUNITY_LOGO"></a><a id="cert_retrieve_community_logo"></a><dl>
<dt><b>CERT_RETRIEVE_COMMUNITY_LOGO</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the certificate community logotype.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RETRIEVE_BIOMETRIC_PICTURE_TYPE"></a><a id="cert_retrieve_biometric_picture_type"></a><dl>
<dt><b>CERT_RETRIEVE_BIOMETRIC_PICTURE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the picture associated with the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RETRIEVE_BIOMETRIC_SIGNATURE_TYPE"></a><a id="cert_retrieve_biometric_signature_type"></a><dl>
<dt><b>CERT_RETRIEVE_BIOMETRIC_SIGNATURE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the signature associated with the certificate.

</td>
</tr>
</table>

### -param dwRetrievalFlags [in]

A set of flags that specify how the information should be retrieved. This parameter is passed as the <i>dwRetrievalFlags</i> in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> function.

### -param dwTimeout [in]

The maximum amount of time, in milliseconds, to wait for the retrieval.

### -param dwFlags [in]

This parameter is not used and must be zero.

### -param pvReserved

This parameter is not used and must be <b>NULL</b>.

### -param ppbData [out]

The address of a <b>BYTE</b> pointer that receives the logotype or biometric data. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

### -param pcbData [out]

The address of a <b>DWORD</b> variable that receives the number of bytes in the <i>ppbData</i> buffer.

### -param ppwszMimeType [out]

The address of a pointer to a null-terminated Unicode string that receives the Multipurpose Internet Mail Extensions (MIME) type of the data. This parameter can be <b>NULL</b> if this information is not needed. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

This address always receives <b>NULL</b> for biometric types. You must always ensure that this parameter contains a valid memory address before attempting to access the memory.

## -returns

Returns nonzero if successful or zero otherwise.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes returned by the 
		       <b>GetLastError</b> function include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> CRYPT_E_HASH_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The computed hash value does not match the hash value in the certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The certificate does not contain the <b>szOID_LOGOTYPE_EXT</b> or <b>szOID_BIOMETRIC_EXT</b> extension, or the specified <i>lpszLogoOrBiometricType</i> was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
No data could be retrieved from the URL specified by the certificate extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The certificate does not support the required extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The hash algorithm OID is unknown.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a>