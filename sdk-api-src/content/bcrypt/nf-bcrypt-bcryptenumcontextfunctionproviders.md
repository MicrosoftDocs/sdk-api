---
UID: NF:bcrypt.BCryptEnumContextFunctionProviders
title: BCryptEnumContextFunctionProviders function (bcrypt.h)
description: Obtains the providers for the cryptographic functions for a context in the specified configuration table.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptEnumContextFunctionProviders","BCryptEnumContextFunctionProviders function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","bcrypt/BCryptEnumContextFunctionProviders","security.bcryptenumcontextfunctionproviders"]
old-location: security\bcryptenumcontextfunctionproviders.htm
tech.root: security
ms.assetid: 82776e61-03bb-463b-8767-fa4f70fe1341
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptEnumContextFunctionProviders, BCryptEnumContextFunctionProviders function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, bcrypt/BCryptEnumContextFunctionProviders, security.bcryptenumcontextfunctionproviders
req.header: bcrypt.h
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptEnumContextFunctionProviders
 - bcrypt/BCryptEnumContextFunctionProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptEnumContextFunctionProviders
---

# BCryptEnumContextFunctionProviders function


## -description

The <b>BCryptEnumContextFunctionProviders</b> function obtains the providers for the cryptographic functions for a context in the specified configuration table.

## -parameters

### -param dwTable [in]

Identifies the configuration table from which to retrieve the context function providers. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LOCAL"></a><a id="crypt_local"></a><dl>
<dt><b>CRYPT_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the context functions from the local-machine configuration table.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DOMAIN"></a><a id="crypt_domain"></a><dl>
<dt><b>CRYPT_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
This value is not available for use.

</td>
</tr>
</table>

### -param pszContext [in]

A pointer to a null-terminated Unicode string that contains the identifier of the context to enumerate the function providers for.

### -param dwInterface [in]

Identifies the cryptographic interface to retrieve the function providers for. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></a><a id="bcrypt_asymmetric_encryption_interface"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the asymmetric encryption function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the cipher function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the <a href="/windows/desktop/SecGloss/h-gly">hash</a> function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the random number generator function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the secret agreement function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the signature function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the key storage function providers.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the Schannel function providers.

</td>
</tr>
</table>

### -param pszFunction [in]

A pointer to a null-terminated Unicode string that contains the identifier of the function to enumerate the providers for.

### -param pcbBuffer [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppBuffer</i>. If this size is not large enough to hold the set of context identifiers, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this value contains the number of bytes that were copied to the <i>ppBuffer</i> buffer.

### -param ppBuffer [in, out]

The address of a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_providers">CRYPT_CONTEXT_FUNCTION_PROVIDERS</a> structure that receives the set of context function providers retrieved by this function. The value pointed to by the <i>pcbBuffer</i> parameter contains the size of this buffer.

If the value pointed to by this parameter is <b>NULL</b>, this function will allocate the required memory. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the variable pointed to by the <i>pcbBuffer</i> parameter and return <b>STATUS_BUFFER_TOO_SMALL</b>.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppBuffer</i> parameter is not <b>NULL</b>, and the value pointed to by the <i>pcbBuffer</i> parameter is not large enough to hold the set of contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No context function providers that match the specified criteria were found.

</td>
</tr>
</table>

## -remarks

<b>BCryptEnumContextFunctionProviders</b> can be called only in user mode.


#### Examples

The following  example shows how to use the <b>BCryptEnumContextFunctionProviders</b> function to enumerate the providers for all key storage functions for all contexts in the local-machine configuration table.


```cpp
#include <windows.h>
#include <stdio.h>
#include <ntstatus.h>
#include <Bcrypt.h>
#pragma comment(lib, "Bcrypt.lib")

#ifndef NT_SUCCESS
#define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
#endif

NTSTATUS EnumContextFunctionProviders()
{
    NTSTATUS status;
    ULONG uSize = 0;
    ULONG uTable = CRYPT_LOCAL;
    PCRYPT_CONTEXTS pContexts = NULL;
    
    // Get the contexts for the local machine. 
    // CNG will allocate the memory for us.
    status = BCryptEnumContexts(uTable, &uSize, &pContexts);
    if(NT_SUCCESS(status))
    {
        // Enumerate the context identifiers.
        for(ULONG a = 0; 
            a < pContexts->cContexts; 
            a++)
        {
            ULONG uInterface = NCRYPT_SCHANNEL_INTERFACE;

            wprintf(L"Context functions for %s:\n", 
                pContexts->rgpszContexts[a]);

            // Get the functions for this context.
            // CNG will allocate the memory for us.
            PCRYPT_CONTEXT_FUNCTIONS pContextFunctions = NULL;
            status = BCryptEnumContextFunctions(
                uTable, 
                pContexts->rgpszContexts[a], 
                uInterface, 
                &uSize, 
                &pContextFunctions);
            if(NT_SUCCESS(status))
            {
                // Enumerate the functions.
                for(ULONG b = 0; 
                    b < pContextFunctions->cFunctions; 
                    b++)
                {
                    wprintf(L"\tFunction providers for %s:\n", 
                        pContextFunctions->rgpszFunctions[b]);

                    // Get the providers for this function.
                    PCRYPT_CONTEXT_FUNCTION_PROVIDERS pProviders;
                    pProviders = NULL;
                    status = BCryptEnumContextFunctionProviders(
                        uTable, 
                        pContexts->rgpszContexts[a], 
                        uInterface, 
                        pContextFunctions->rgpszFunctions[b],
                        &uSize, 
                        &pProviders);
                    if(NT_SUCCESS(status))
                    {
                        for(ULONG c = 0; 
                            c < pProviders->cProviders; 
                            c++)
                        {
                            wprintf(L"\t\t%s\n", 
                                pProviders->rgpszProviders[c]);
                        }
                    }
                    else if(STATUS_NOT_FOUND == status)
                    {
                        wprintf(L"\t\tNone found.\n");
                    }
                }

                // Free the context functions buffer.
                BCryptFreeBuffer(pContextFunctions);
            }
        }

        // Free the contexts buffer.
        BCryptFreeBuffer(pContexts);
    }

    return status;
}

```

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_providers">CRYPT_CONTEXT_FUNCTION_PROVIDERS</a>