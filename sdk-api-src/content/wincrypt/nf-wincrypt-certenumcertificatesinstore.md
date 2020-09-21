---
UID: NF:wincrypt.CertEnumCertificatesInStore
title: CertEnumCertificatesInStore function (wincrypt.h)
description: Retrieves the first or next certificate in a certificate store. Used in a loop, this function can retrieve in sequence all certificates in a certificate store.
helpviewer_keywords: ["CertEnumCertificatesInStore","CertEnumCertificatesInStore function [Security]","_crypto2_certenumcertificatesinstore","security.certenumcertificatesinstore","wincrypt/CertEnumCertificatesInStore"]
old-location: security\certenumcertificatesinstore.htm
tech.root: security
ms.assetid: c5ab5b4c-dc0c-416b-aa9e-b939398cfa6d
ms.date: 12/05/2018
ms.keywords: CertEnumCertificatesInStore, CertEnumCertificatesInStore function [Security], _crypto2_certenumcertificatesinstore, security.certenumcertificatesinstore, wincrypt/CertEnumCertificatesInStore
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
 - CertEnumCertificatesInStore
 - wincrypt/CertEnumCertificatesInStore
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
 - CertEnumCertificatesInStore
---

# CertEnumCertificatesInStore function


## -description

The <b>CertEnumCertificatesInStore</b> function retrieves the first or next certificate in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. Used in a loop, this function can retrieve in sequence all certificates in a certificate store.

## -parameters

### -param hCertStore [in]

A handle of a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param pPrevCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the previous <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> found.

This parameter must be <b>NULL</b> to begin the enumeration and get the first certificate in the store. Successive certificates are enumerated by setting <i>pPrevCertContext</i> to the pointer returned by a previous call to the function. This function frees the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> referenced by non-<b>NULL</b> values of this parameter.

For <a href="/windows/desktop/SecGloss/l-gly">logical stores</a>, including collection stores, a duplicate of the <i>pCertContext</i> returned by this function cannot be used to begin a new subsequence of enumerations because the duplicated certificate loses the initial enumeration <a href="/windows/desktop/SecGloss/s-gly">state</a>. The enumeration skips any certificate previously deleted by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecertificatefromstore">CertDeleteCertificateFromStore</a>.

## -returns

If the function succeeds, the function returns  a pointer to the next 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> in the store. If no more certificates exist in the store, the function returns <b>NULL</b>.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the certificate context pointed to by <i>pPrevCertContext</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND </b></dt>
</dl>
</td>
<td width="60%">
No certificates were found. This happens if the store is empty or if the function reached the end of the store's list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_FILES</b></dt>
</dl>
</td>
<td width="60%">
Applies to external stores. No certificates were found. This happens if the store is empty or if the function reached the end of the store's list.

</td>
</tr>
</table>

## -remarks

The returned pointer is freed when passed as the <i>pPrevCertContext</i> parameter on a subsequent call. Otherwise, the pointer must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. A non-<b>NULL</b> <i>pPrevCertContext</i> passed to <b>CertEnumCertificatesInStore</b> is always freed even for an error.

A duplicate of the currently enumerated certificate can be made by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>.


#### Examples

The following  example lists the certificate contexts in the certificate store. For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-deleting-certificates-from-a-certificate-store">Example C Program: Deleting Certificates from a Certificate Store</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>
#pragma comment(lib, "crypt32.lib")


//--------------------------------------------------------------------
// Declare and initialize variables.
HANDLE          hStoreHandle = NULL;
PCCERT_CONTEXT  pCertContext = NULL;   
char * pszStoreName = "CA";

//--------------------------------------------------------------------
// Open a system certificate store.
if (hStoreHandle = CertOpenSystemStore(
     NULL,     
     pszStoreName))
    {
         printf("The %s store has been opened. \n", pszStoreName);
    }
    else
    {
         printf("The store was not opened.\n");
         exit(1);
    }

//-------------------------------------------------------------------
// Find the certificates in the system store. 
while(pCertContext= CertEnumCertificatesInStore(
      hStoreHandle,
      pCertContext)) // on the first call to the function,
                     // this parameter is NULL 
                     // on all subsequent calls, 
                     // this parameter is the last pointer 
                     // returned by the function
{
    //----------------------------------------------------------------
    // Do whatever is needed for a current certificate.
    // ...
} // End of while.

//--------------------------------------------------------------------
//   Clean up.
if (!CertCloseStore(
         hStoreHandle,
         0))
{
    printf("Failed CertCloseStore\n");
    exit(1);
}

```

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecertificatefromstore">CertDeleteCertificateFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcrlinstore">CertFindCRLInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>