---
UID: NF:wincrypt.CertSaveStore
title: CertSaveStore function (wincrypt.h)
description: Saves the certificate store to a file or to a memory BLOB.
helpviewer_keywords: ["CERT_STORE_SAVE_AS_PKCS7","CERT_STORE_SAVE_AS_STORE","CERT_STORE_SAVE_TO_FILE","CERT_STORE_SAVE_TO_FILENAME","CERT_STORE_SAVE_TO_FILENAME_A","CERT_STORE_SAVE_TO_FILENAME_W","CERT_STORE_SAVE_TO_MEMORY","CertSaveStore","CertSaveStore function [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","_crypto2_certsavestore","security.certsavestore","wincrypt/CertSaveStore"]
old-location: security\certsavestore.htm
tech.root: security
ms.assetid: 5cc818d7-b079-4962-aabc-fc512d4e92ac
ms.date: 12/05/2018
ms.keywords: CERT_STORE_SAVE_AS_PKCS7, CERT_STORE_SAVE_AS_STORE, CERT_STORE_SAVE_TO_FILE, CERT_STORE_SAVE_TO_FILENAME, CERT_STORE_SAVE_TO_FILENAME_A, CERT_STORE_SAVE_TO_FILENAME_W, CERT_STORE_SAVE_TO_MEMORY, CertSaveStore, CertSaveStore function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, _crypto2_certsavestore, security.certsavestore, wincrypt/CertSaveStore
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
 - CertSaveStore
 - wincrypt/CertSaveStore
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
 - CertSaveStore
---

# CertSaveStore function


## -description

The <b>CertSaveStore</b> function saves the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> to a file or to a memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

## -parameters

### -param hCertStore [in]

The handle of the certificate store to be saved.

### -param dwEncodingType [in]

Specifies the <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a> and <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a>. Encoding is used only when <i>dwSaveAs</i> contains <b>CERT_STORE_SAVE_AS_PKCS7</b>. Otherwise, the <i>dwMsgAndCertEncodingType</i> parameter is not used.


This parameter can be a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PKCS_7_ASN_ENCODING"></a><a id="pkcs_7_asn_encoding"></a><dl>
<dt><b>PKCS_7_ASN_ENCODING</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
Specifies PKCS 7 message encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies X.509 certificate encoding.

</td>
</tr>
</table>

### -param dwSaveAs [in]

Specifies how to save the certificate store.


This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_AS_PKCS7"></a><a id="cert_store_save_as_pkcs7"></a><dl>
<dt><b>CERT_STORE_SAVE_AS_PKCS7</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The certificate store can be saved as a <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> signed message that does not include additional properties. The <i>dwEncodingType</i> parameter specifies the message encoding type.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_AS_STORE"></a><a id="cert_store_save_as_store"></a><dl>
<dt><b>CERT_STORE_SAVE_AS_STORE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The certificate store can be saved as a serialized store containing properties in addition to encoded certificates, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs), and <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs). The <i>dwEncodingType</i> parameter is ignored.

<div class="alert"><b>Note</b>  The <b>CERT_KEY_CONTEXT_PROP_ID</b> property and the related <b>CERT_KEY_PROV_HANDLE_PROP_ID</b> and <b>CERT_KEY_SPEC_PROP_ID</b> values are not saved to a serialized store.</div>
<div> </div>
</td>
</tr>
</table>

### -param dwSaveTo [in]

Specifies where and how to save the certificate store. The contents of this parameter determines the format of the <i>pvSaveToPara</i> parameter.


This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_TO_FILE"></a><a id="cert_store_save_to_file"></a><dl>
<dt><b>CERT_STORE_SAVE_TO_FILE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The function saves the certificate store to a file. The <i>pvSaveToPara</i> parameter contains a handle to a file previously obtained by using the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. The file must be opened with write permission. After a successful save operation, the file pointer is positioned after the last write operation.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_TO_FILENAME"></a><a id="cert_store_save_to_filename"></a><dl>
<dt><b>CERT_STORE_SAVE_TO_FILENAME</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The function saves the certificate store to a file. The <i>pvSaveToPara</i> parameter contains a pointer to a null-terminated Unicode string that contains the path and file name of the file to save to. The function opens the file, saves to it, and closes it.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_TO_FILENAME_A"></a><a id="cert_store_save_to_filename_a"></a><dl>
<dt><b>CERT_STORE_SAVE_TO_FILENAME_A</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The function saves the certificate store to a file. The <i>pvSaveToPara</i> parameter contains a pointer to a null-terminated ANSI string that contains the path and file name of the file to save to. The function opens the file, saves to it, and closes it.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_TO_FILENAME_W"></a><a id="cert_store_save_to_filename_w"></a><dl>
<dt><b>CERT_STORE_SAVE_TO_FILENAME_W</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The function saves the certificate store to a file. The <i>pvSaveToPara</i> parameter contains a pointer to a null-terminated Unicode string that contains the path and file name of the file to save to. The function opens the file, saves to it, and closes it.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SAVE_TO_MEMORY"></a><a id="cert_store_save_to_memory"></a><dl>
<dt><b>CERT_STORE_SAVE_TO_MEMORY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The function saves the certificate store to a memory BLOB. The <i>pvSaveToPara</i> parameter contains a pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> structure. Before use, the <b>CERT_BLOB</b>'s <b>pbData</b> and <b>cbData</b> members must be initialized. Upon return, <b>cbData</b> is updated with the actual length. For a length-only calculation, <b>pbData</b> must be set to <b>NULL</b>. If <b>pbData</b> is non-<b>NULL</b> and <b>cbData</b> is not large enough, the function returns zero with a last error code of <b>ERROR_MORE_DATA</b>.

</td>
</tr>
</table>

### -param pvSaveToPara [in, out]

A pointer that represents where the store should be saved to. The contents of this parameter depends on the value of the <i>dwSaveTo</i> parameter.

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Note that <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> errors can be propagated to this function. One possible error code is <b>CRYPT_E_FILE_ERROR</b> which indicates that an error occurred while writing to the file.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>