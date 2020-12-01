---
UID: NF:bcrypt.BCryptEnumContextFunctions
title: BCryptEnumContextFunctions function (bcrypt.h)
description: Obtains the cryptographic functions for a context in the specified configuration table.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptEnumContextFunctions","BCryptEnumContextFunctions function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","bcrypt/BCryptEnumContextFunctions","security.bcryptenumcontextfunctions"]
old-location: security\bcryptenumcontextfunctions.htm
tech.root: security
ms.assetid: 81bdfd47-7001-4e63-a8b3-33dae99f2c66
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptEnumContextFunctions, BCryptEnumContextFunctions function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, bcrypt/BCryptEnumContextFunctions, security.bcryptenumcontextfunctions
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
 - BCryptEnumContextFunctions
 - bcrypt/BCryptEnumContextFunctions
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
 - BCryptEnumContextFunctions
---

# BCryptEnumContextFunctions function


## -description

The <b>BCryptEnumContextFunctions</b> function obtains the cryptographic functions for a context in the specified configuration table.

## -parameters

### -param dwTable [in]

Identifies the configuration table from which to retrieve the context functions. This can be one of the following values.

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

A pointer to a null-terminated Unicode string that contains the identifier of the context to enumerate the functions for.

### -param dwInterface [in]

Identifies the cryptographic interface to retrieve the functions for. This can be one of the following values.

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
Retrieve the asymmetric encryption functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the cipher functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the hash functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the random number generator functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the secret agreement functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the signature functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the key storage functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the Schannel functions.

</td>
</tr>
</table>

### -param pcbBuffer [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppBuffer</i>. If this size is not large enough to hold the set of context identifiers, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this value contains the number of bytes that were copied to the <i>ppBuffer</i> buffer.

### -param ppBuffer [in, out]

The address of a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_functions">CRYPT_CONTEXT_FUNCTIONS</a> structure that receives the set of context functions retrieved by this function. The value pointed to by the <i>pcbBuffer</i> parameter contains the size of this buffer.

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
No context functions that match the specified criteria were found.

</td>
</tr>
</table>

## -remarks

<b>BCryptEnumContextFunctions</b> can be called only in user mode.


#### Examples

The following example shows how to use the <b>BCryptEnumContextFunctions</b> function to enumerate the key storage functions for all contexts in the local-machine configuration table.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Bcrypt.h>
#pragma comment(lib, "Bcrypt.lib")

#ifndef NT_SUCCESS
#define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
#endif

NTSTATUS EnumContextFunctions()
{
    NTSTATUS status;
    ULONG uSize = 0;
    PCRYPT_CONTEXTS pContexts = NULL;
    
    // Get the contexts for the local machine. 
    // CNG will allocate the memory for us.
    status = BCryptEnumContexts(CRYPT_LOCAL, &uSize, &pContexts);
    if(NT_SUCCESS(status))
    {
        // Enumerate the context identifiers.
        for(ULONG uContextIndex = 0; 
            uContextIndex < pContexts->cContexts; 
            uContextIndex++)
        {
            wprintf(L"Context functions for %s:\n", 
                pContexts->rgpszContexts[uContextIndex]);

            // Get the functions for this context.
            // CNG will allocate the memory for us.
            PCRYPT_CONTEXT_FUNCTIONS pContextFunctions = NULL;
            status = BCryptEnumContextFunctions(
                CRYPT_LOCAL, 
                pContexts->rgpszContexts[uContextIndex], 
                NCRYPT_SCHANNEL_INTERFACE, 
                &uSize, 
                &pContextFunctions);
            if(NT_SUCCESS(status))
            {
                // Enumerate the functions.
                for(ULONG i = 0; 
                    i < pContextFunctions->cFunctions; 
                    i++)
                {
                    wprintf(L"\t%s\n", 
                        pContextFunctions->rgpszFunctions[i]);
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

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_functions">CRYPT_CONTEXT_FUNCTIONS</a>