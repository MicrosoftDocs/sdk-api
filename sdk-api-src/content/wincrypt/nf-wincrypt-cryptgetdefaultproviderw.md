---
UID: NF:wincrypt.CryptGetDefaultProviderW
title: CryptGetDefaultProviderW function (wincrypt.h)
description: Finds the default cryptographic service provider (CSP) of a specified provider type for the local computer or current user. (Unicode)
helpviewer_keywords: ["CRYPT_MACHINE_DEFAULT", "CRYPT_USER_DEFAULT", "CryptGetDefaultProvider", "CryptGetDefaultProvider function [Security]", "CryptGetDefaultProviderW", "_crypto2_cryptgetdefaultprovider", "security.cryptgetdefaultprovider", "wincrypt/CryptGetDefaultProvider", "wincrypt/CryptGetDefaultProviderW"]
old-location: security\cryptgetdefaultprovider.htm
tech.root: security
ms.assetid: 5d15641e-1ad7-441d-9423-65fd51de9812
ms.date: 12/05/2018
ms.keywords: CRYPT_MACHINE_DEFAULT, CRYPT_USER_DEFAULT, CryptGetDefaultProvider, CryptGetDefaultProvider function [Security], CryptGetDefaultProviderA, CryptGetDefaultProviderW, _crypto2_cryptgetdefaultprovider, security.cryptgetdefaultprovider, wincrypt/CryptGetDefaultProvider, wincrypt/CryptGetDefaultProviderA, wincrypt/CryptGetDefaultProviderW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptGetDefaultProviderW (Unicode) and CryptGetDefaultProviderA (ANSI)
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
 - CryptGetDefaultProviderW
 - wincrypt/CryptGetDefaultProviderW
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
 - CryptGetDefaultProvider
 - CryptGetDefaultProviderA
 - CryptGetDefaultProviderW
---

# CryptGetDefaultProviderW function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGetDefaultProvider</b> function finds the default <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) of a specified provider type for the local computer or current user. The name of the default CSP for the provider type specified in the <i>dwProvType</i> parameter is returned in the <i>pszProvName</i> buffer.

## -parameters

### -param dwProvType [in]

The provider type for which the default CSP name is to be found. 

Defined provider types are  as follows:

<ul>
<li>
<a href="/windows/desktop/SecCrypto/prov-rsa-full">PROV_RSA_FULL</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-rsa-sig">PROV_RSA_SIG</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-dss">PROV_DSS</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-dss-dh">PROV_DSS_DH</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-dh-schannel">PROV_DH_SCHANNEL</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-fortezza">PROV_FORTEZZA</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-ms-exchange">PROV_MS_EXCHANGE</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-rsa-schannel">PROV_RSA_SCHANNEL</a>
</li>
<li>
<a href="/windows/desktop/SecCrypto/prov-ssl">PROV_SSL</a>
</li>
</ul>

### -param pdwReserved [in]

This parameter is reserved for future use and must be <b>NULL</b>.

### -param dwFlags [in]

The following flag values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_DEFAULT"></a><a id="crypt_user_default"></a><dl>
<dt><b>CRYPT_USER_DEFAULT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns the user-context default CSP of the specified type.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_DEFAULT"></a><a id="crypt_machine_default"></a><dl>
<dt><b>CRYPT_MACHINE_DEFAULT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Returns the computer default CSP of the specified type.

</td>
</tr>
</table>

### -param pszProvName [out]

A pointer to a null-terminated character string buffer to receive the name of the default CSP.

To find the size of the buffer for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbProvName [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the buffer pointed to by the <i>pszProvName</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored or to be stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).
						

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error code prefaced by NTE is generated by the particular CSP being used. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The buffer for the name is not large enough.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter has an unrecognized value.

</td>
</tr>
</table>

## -remarks

This function determines which installed CSP is currently set as the default for the local computer or current user. This information is often displayed to the user.


#### Examples

The following example retrieves the name of the default CSP for the PROV_RSA_FULL provider type. For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-enumerating-csp-providers-and-provider-types">Example C Program: Enumerating CSP Providers and Provider Types</a>.


```cpp
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#pragma comment(lib, "crypt32.lib")

void main()
{

    DWORD       cbProvName=0;
    LPTSTR      pbProvName=NULL;
    // Copyright (C) Microsoft.  All rights reserved.
    // Get the length of the RSA_FULL default provider name.
    if (!(CryptGetDefaultProvider(
         PROV_RSA_FULL, 
         NULL, 
         CRYPT_MACHINE_DEFAULT,
         NULL, 
         &cbProvName))) 
    { 
      printf("Error getting the length of the default "
          "provider name.\n");
      exit(1);
    }

    // Allocate local memory for the name of the default provider.
    if (!(pbProvName = (LPTSTR)LocalAlloc(LMEM_ZEROINIT, 
        cbProvName)))
    {
        printf("Error during memory allocation for "
            "provider name.\n");
        exit(1);
    }

    // Get the default provider name.
    if (CryptGetDefaultProvider(
        PROV_RSA_FULL, 
        NULL, 
        CRYPT_MACHINE_DEFAULT,
        pbProvName,
        &cbProvName)) 
    {
        printf("The default provider name is %s\n",pbProvName);
    }
    else
    {
        printf("Getting the name of the provider failed.\n");
        exit(1);
    }

    // Free resources when done.
    LocalFree(pbProvName);

}

```






> [!NOTE]
> The wincrypt.h header defines CryptGetDefaultProvider as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovidera">CryptSetProvider</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetproviderexa">CryptSetProviderEx</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>
