---
UID: NF:wincrypt.CertAddEncodedCertificateToSystemStoreA
title: CertAddEncodedCertificateToSystemStoreA function (wincrypt.h)
description: Opens the specified system store and adds the encoded certificate to it. (ANSI)
helpviewer_keywords: ["CertAddEncodedCertificateToSystemStoreA", "wincrypt/CertAddEncodedCertificateToSystemStoreA"]
old-location: security\certaddencodedcertificatetosystemstore.htm
tech.root: security
ms.assetid: 72ff1bcc-eb94-4d97-89fa-d95ed9eb460e
ms.date: 12/05/2018
ms.keywords: CertAddEncodedCertificateToSystemStore, CertAddEncodedCertificateToSystemStore function [Security], CertAddEncodedCertificateToSystemStoreA, CertAddEncodedCertificateToSystemStoreW, security.certaddencodedcertificatetosystemstore, wincrypt/CertAddEncodedCertificateToSystemStore, wincrypt/CertAddEncodedCertificateToSystemStoreA, wincrypt/CertAddEncodedCertificateToSystemStoreW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertAddEncodedCertificateToSystemStoreW (Unicode) and CertAddEncodedCertificateToSystemStoreA (ANSI)
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
 - CertAddEncodedCertificateToSystemStoreA
 - wincrypt/CertAddEncodedCertificateToSystemStoreA
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
 - CertAddEncodedCertificateToSystemStore
 - CertAddEncodedCertificateToSystemStoreA
 - CertAddEncodedCertificateToSystemStoreW
---

# CertAddEncodedCertificateToSystemStoreA function


## -description

The <b>CertAddEncodedCertificateToSystemStore</b> function opens the specified system store and adds the encoded certificate to it.

## -parameters

### -param szCertStoreName [in]

A null-terminated string that contains the name of the system store for the encoded certificate.

### -param pbCertEncoded [in]

A pointer to a buffer that contains the encoded certificate to add.

### -param cbCertEncoded [in]

The size, in bytes, of the <i>pbCertEncoded</i> buffer.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. <b>CertAddEncodedCertificateToSystemStore</b> depends on the functions listed in the following remarks for error handling. Refer to those function topics for their respective error handling behaviors. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Internally, <b>CertAddEncodedCertificateToSystemStore</b> calls <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a> with the following parameters.


<table>
<tr>
<th>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> Parameter</th>
<th>Value</th>
</tr>
<tr>
<td><i>szSubsystemProtocol</i></td>
<td><i>szCertStoreName</i></td>
</tr>
</table>
 



If <b>CertAddEncodedCertificateToSystemStore</b> obtains a handle to the specified system store, it calls <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> to close the handle before it returns.


<table>
<tr>
<th>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a> Parameter</th>
<th>Value</th>
</tr>
<tr>
<td><i>dwCertEncodingType</i></td>
<td><b>X509_ASN_ENCODING</b></td>
</tr>
<tr>
<td><i>dwAddDisposition</i></td>
<td><b>CERT_STORE_ADD_USE_EXISTING</b></td>
</tr>
<tr>
<td><i>ppCertContext</i></td>
<td><b>NULL</b></td>
</tr>
</table>
 






> [!NOTE]
> The wincrypt.h header defines CertAddEncodedCertificateToSystemStore as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
