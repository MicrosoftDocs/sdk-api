---
UID: NF:bcrypt.BCryptEnumContexts
title: BCryptEnumContexts function (bcrypt.h)
description: Obtains the identifiers of the contexts in the specified configuration table.
helpviewer_keywords: ["BCryptEnumContexts","BCryptEnumContexts function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","bcrypt/BCryptEnumContexts","security.bcryptenumcontexts"]
old-location: security\bcryptenumcontexts.htm
tech.root: security
ms.assetid: 02646a80-6e93-4169-83da-0488ff3da56f
ms.date: 12/05/2018
ms.keywords: BCryptEnumContexts, BCryptEnumContexts function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, bcrypt/BCryptEnumContexts, security.bcryptenumcontexts
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
 - BCryptEnumContexts
 - bcrypt/BCryptEnumContexts
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
 - BCryptEnumContexts
---

# BCryptEnumContexts function


## -description

<p class="CCE_Message">[<b>BCryptEnumContexts</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>BCryptEnumContexts</b> function obtains the identifiers of the contexts in the specified configuration table.

## -parameters

### -param dwTable [in]

Identifies the configuration table from which to retrieve the contexts. This can be one of the following values.

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
Retrieve the contexts from the local-machine configuration table.

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

### -param pcbBuffer [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppBuffer</i>. If this size is not large enough to hold the set of context identifiers, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this value contains the number of bytes that were copied to the <i>ppBuffer</i> buffer.

### -param ppBuffer [in, out]

The address of a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_contexts">CRYPT_CONTEXTS</a> structure that receives the set of contexts retrieved by this function. The value pointed to by the <i>pcbBuffer</i> parameter contains the size of this buffer.

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
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppBuffer</i> parameter is not <b>NULL</b>, and the value pointed to by the <i>pcbBuffer</i> parameter is not large enough to hold the set of contexts.

</td>
</tr>
</table>

## -remarks

<b>BCryptEnumContexts</b> can be called only in user mode.


#### Examples

The following example shows how to use the <b>BCryptEnumContexts</b> function to allocate the memory for the <i>ppBuffer</i> buffer.


```cpp
#ifndef NT_SUCCESS
#define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
#endif

NTSTATUS EnumContexts_SystemAlloc()
{
    NTSTATUS status;
    ULONG uSize = 0;
    PCRYPT_CONTEXTS pContexts = NULL;
    
    // Get the contexts for the local computer. 
    // CNG allocates the memory.
    status = BCryptEnumContexts(CRYPT_LOCAL, &uSize, &pContexts);
    if(NT_SUCCESS(status))
    {
        // Enumerate the context identifiers.
        for(ULONG i = 0; i < pContexts->cContexts; i++)
        {
            wprintf(pContexts->rgpszContexts[i]);
            wprintf(L"\n");
        }

        // Free the buffer.
        BCryptFreeBuffer(pContexts);
    }

    return status;
}

```


The following example shows how to use the <b>BCryptEnumContexts</b> function to allocate your own memory for the <i>ppBuffer</i> buffer.


```cpp
#ifndef NT_SUCCESS
#define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
#endif

NTSTATUS EnumContexts_SelfAlloc()
{
    NTSTATUS status;
    ULONG uSize = 0;
    
    // Get the required size of the buffer.
    status = BCryptEnumContexts(CRYPT_LOCAL, &uSize, NULL);
    if(STATUS_BUFFER_TOO_SMALL == status)
    {
        // Allocate the buffer.
        PCRYPT_CONTEXTS pContexts = (PCRYPT_CONTEXTS)HeapAlloc(
            GetProcessHeap(), 
            HEAP_ZERO_MEMORY, 
            uSize);
        if(pContexts)
        {
            // Get the contexts for the local machine.
            status = BCryptEnumContexts(
                CRYPT_LOCAL, 
                &uSize, 
                &pContexts);
            if(NT_SUCCESS((status))
            {
                // Enumerate the context identifiers.
                for(ULONG i = 0; i < pContexts->cContexts; i++)
                {
                    wprintf(pContexts->rgpszContexts[i]);
                    wprintf(L"\n");
                }
            }

            // Free the buffer.
            HeapFree(GetProcessHeap(), 0, pContexts);
            pContexts = NULL;
        }
        else
        {
            status = STATUS_NO_MEMORY;
        }
    }

    return status;
}

```

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_contexts">CRYPT_CONTEXTS</a>