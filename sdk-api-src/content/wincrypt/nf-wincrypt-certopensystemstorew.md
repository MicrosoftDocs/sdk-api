---
UID: NF:wincrypt.CertOpenSystemStoreW
title: CertOpenSystemStoreW function (wincrypt.h)
description: Opens the most common system certificate store. To open certificate stores with more complex requirements, such as file-based or memory-based stores, use CertOpenStore. (Unicode)
helpviewer_keywords: ["CA", "CertOpenSystemStore", "CertOpenSystemStore function [Security]", "CertOpenSystemStoreW", "MY", "ROOT", "SPC", "_crypto2_certopensystemstore", "security.certopensystemstore", "wincrypt/CertOpenSystemStore", "wincrypt/CertOpenSystemStoreW"]
old-location: security\certopensystemstore.htm
tech.root: security
ms.assetid: 23699439-1a6c-4907-93fa-651024856be7
ms.date: 12/05/2018
ms.keywords: CA, CertOpenSystemStore, CertOpenSystemStore function [Security], CertOpenSystemStoreA, CertOpenSystemStoreW, MY, ROOT, SPC, _crypto2_certopensystemstore, security.certopensystemstore, wincrypt/CertOpenSystemStore, wincrypt/CertOpenSystemStoreA, wincrypt/CertOpenSystemStoreW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertOpenSystemStoreW (Unicode) and CertOpenSystemStoreA (ANSI)
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
 - CertOpenSystemStoreW
 - wincrypt/CertOpenSystemStoreW
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
 - CertOpenSystemStore
 - CertOpenSystemStoreA
 - CertOpenSystemStoreW
---

# CertOpenSystemStoreW function


## -description

The <b>CertOpenSystemStore</b> function is a simplified function that opens the most common system <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. To open certificate stores with more complex requirements, such as file-based or memory-based stores, use <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>.

## -parameters

### -param hProv [in]

This parameter is not used and should be set to <b>0</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle of a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). Set <i>hProv</i> to <b>0</b> to use the default CSP. If <i>hProv</i> is not <b>0</b>, it must be a CSP handle created by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function.This parameter's data type is <b>HCRYPTPROV</b>.

### -param szSubsystemProtocol [in]

A string that names a system store. If the system store name provided in this parameter is not the name of an existing system store, a new system store will be created and used. <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstore">CertEnumSystemStore</a> can be used to list the names of existing system stores. Some example system stores are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CA"></a><a id="ca"></a><dl>
<dt><b>CA</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/c-gly">Certification authority</a> certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="MY"></a><a id="my"></a><dl>
<dt><b>MY</b></dt>
</dl>
</td>
<td width="60%">
A certificate store that holds certificates with associated private keys.

</td>
</tr>
<tr>
<td width="40%"><a id="ROOT"></a><a id="root"></a><dl>
<dt><b>ROOT</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/r-gly">Root certificates</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SPC"></a><a id="spc"></a><dl>
<dt><b>SPC</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/s-gly">Software Publisher Certificate</a>.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns a handle to the certificate store.

If the function fails, it returns <b>NULL</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called function <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> are propagated to this function.</div>
<div> </div>

## -remarks

Only current user certificates are accessible using this method, not the local machine store.

After the system store is opened, all the standard certificate store functions can be used to manipulate the certificates.

After use, the store should be closed by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>.

For more information about the stores that are automatically migrated, see <a href="/windows/desktop/SecCrypto/certificate-store-migration">Certificate Store Migration</a>.


#### Examples

The following example shows a simplified method for opening the most common system certificate stores. For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-certificate-store-operations">Example C Program: Certificate Store Operations</a>.


```cpp
//--------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE  hSystemStore;              // system store handle

//--------------------------------------------------------------------
// Open the CA system certificate store. The same call can be
// used with the name of a different system store, such as My or Root,
// as the second parameter.

if(hSystemStore = CertOpenSystemStore(
    0,
    "CA"))
{
  printf("The CA system store is open. Continue.\n");
}
else
{
  printf("The CA system store did not open.\n");
  exit(1);
}

// Use the store as needed.
// ...

// When done using the store, close it.
if(!CertCloseStore(hSystemStore, 0))
{
  printf("Unable to close the CA system store.\n");
  exit(1);
}
```






> [!NOTE]
> The wincrypt.h header defines CertOpenSystemStore as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsavestore">CertSaveStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>
