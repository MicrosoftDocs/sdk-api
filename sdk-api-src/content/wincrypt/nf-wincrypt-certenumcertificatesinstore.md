---
UID: NF:wincrypt.CertEnumCertificatesInStore
title: CertEnumCertificatesInStore function
author: windows-sdk-content
description: Retrieves the first or next certificate in a certificate store. Used in a loop, this function can retrieve in sequence all certificates in a certificate store.
old-location: security\certenumcertificatesinstore.htm
tech.root: SecCrypto
ms.assetid: c5ab5b4c-dc0c-416b-aa9e-b939398cfa6d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CertEnumCertificatesInStore, CertEnumCertificatesInStore function [Security], _crypto2_certenumcertificatesinstore, security.certenumcertificatesinstore, wincrypt/CertEnumCertificatesInStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertEnumCertificatesInStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertEnumCertificatesInStore function


## -description


The <b>CertEnumCertificatesInStore</b> function retrieves the first or next certificate in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. Used in a loop, this function can retrieve in sequence all certificates in a certificate store.


## -parameters




### -param hCertStore [in]

A handle of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param pPrevCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the previous <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> found.

This parameter must be <b>NULL</b> to begin the enumeration and get the first certificate in the store. Successive certificates are enumerated by setting <i>pPrevCertContext</i> to the pointer returned by a previous call to the function. This function frees the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> referenced by non-<b>NULL</b> values of this parameter.

For <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logical stores</a>, including collection stores, a duplicate of the <i>pCertContext</i> returned by this function cannot be used to begin a new subsequence of enumerations because the duplicated certificate loses the initial enumeration <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>. The enumeration skips any certificate previously deleted by 
<a href="https://msdn.microsoft.com/4390c8da-9c4d-47a4-9af4-d179829f77f3">CertDeleteCertificateFromStore</a>.


## -returns



If the function succeeds, the function returns  a pointer to the next 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> in the store. If no more certificates exist in the store, the function returns <b>NULL</b>.

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

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
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. A non-<b>NULL</b> <i>pPrevCertContext</i> passed to <b>CertEnumCertificatesInStore</b> is always freed even for an error.

A duplicate of the currently enumerated certificate can be made by calling 
<a href="https://msdn.microsoft.com/589edd25-c8d0-4f93-83b2-9df2ed2e2812">CertDuplicateCertificateContext</a>.


#### Examples

The following  example lists the certificate contexts in the certificate store. For another example that uses this function, see <a href="https://msdn.microsoft.com/52a0287b-7d2a-483e-8bbc-43621c4b7103">Example C Program: Deleting Certificates from a Certificate Store</a>.


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




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/4390c8da-9c4d-47a4-9af4-d179829f77f3">CertDeleteCertificateFromStore</a>



<a href="https://msdn.microsoft.com/589edd25-c8d0-4f93-83b2-9df2ed2e2812">CertDuplicateCertificateContext</a>



<a href="https://msdn.microsoft.com/3e481912-204a-4d86-ab67-81f8ae4d1aaa">CertFindCRLInStore</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>



<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="cryptography_functions.htm">Certificate Functions</a>
 

 

