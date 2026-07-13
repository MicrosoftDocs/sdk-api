---
UID: NF:tdh.TdhEnumerateProviderFieldInformation
title: TdhEnumerateProviderFieldInformation function (tdh.h)
description: Retrieves the specified field metadata for a given provider.
old-location: etw\tdhenumerateproviderfieldinformation_func.htm
tech.root: ETW
ms.assetid: ab34a433-b641-4408-81d5-c93609204d24
ms.date: 12/05/2018
ms.keywords: TdhEnumerateProviderFieldInformation, TdhEnumerateProviderFieldInformation function [ETW], etw.tdhenumerateproviderfieldinformation_func, tdh.tdhenumerateproviderfieldinformation_func, tdh/TdhEnumerateProviderFieldInformation
req.header: tdh.h
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
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhEnumerateProviderFieldInformation
 - tdh/TdhEnumerateProviderFieldInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhEnumerateProviderFieldInformation
---

# TdhEnumerateProviderFieldInformation function


## -description

Retrieves the specified field metadata for a given provider.

## -parameters

### -param pGuid [in]

GUID that identifies the provider whose information you want to retrieve.

### -param EventFieldType [in]

Specify the type of field for which you want to retrieve information. For possible values, see the <a href="/windows/desktop/api/tdh/ne-tdh-event_field_type">EVENT_FIELD_TYPE</a> enumeration.

### -param pBuffer [out, optional]

User-allocated buffer to receive the field information. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-provider_field_infoarray">PROVIDER_FIELD_INFOARRAY</a> structure.

### -param pBufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pBuffer</i> buffer is too small. Use the required buffer size set in <i>pBufferSize</i> to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested field type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The manifest or MOF class was not found or does not contain information for the requested field type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>resourceFileName</b> attribute in the manifest contains the location of the provider binary. When you register the manifest, the location is written to the registry. TDH was unable to find the binary based on the registered location.

</td>
</tr>
</table>

## -remarks

This function uses the XML manifest or WMI MOF class to retrieve the information.


#### Examples

The following example shows how to enumerate information contained in the manifest or MOF class for the requested field.


```cpp
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>
#include <tdh.h>

#pragma comment(lib, "tdh.lib")

DWORD EnumFieldInfo(LPGUID pProvider, EVENT_FIELD_TYPE fieldType);

// GUID of the provider whose metadata you want to enumerate.

EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;

    // Retrieve the keyword information.

    wprintf(L"Retrieve EventKeywordInformation\n");

    status = EnumFieldInfo((LPGUID)&ProviderGuid, EventKeywordInformation);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"Failed to retrieve EventKeywordInformation (%lu).\n\n", status);
    }
}

// Prints the information associated with the specified field type.
DWORD EnumFieldInfo(LPGUID pProvider, EVENT_FIELD_TYPE fieldType)
{
    DWORD status = ERROR_SUCCESS;
    PROVIDER_FIELD_INFOARRAY* penum = NULL;
    DWORD bufferSize = 0;

    // Retrieve the required buffer size. If the status is ERROR_INSUFFICIENT_BUFFER,
    // use bufferSize to allocate the buffer.

    status = TdhEnumerateProviderFieldInformation(pProvider, fieldType, penum, &bufferSize);
    if (ERROR_INSUFFICIENT_BUFFER == status)
    {
        penum = (PROVIDER_FIELD_INFOARRAY*) malloc(bufferSize);
        if (penum == NULL)
        {
            wprintf(L"Allocation failed (size=%lu).\n", bufferSize);
            status = ERROR_OUTOFMEMORY;
            goto cleanup;
        }

        // Retrieve the information for the field type.

        status = TdhEnumerateProviderFieldInformation(pProvider, fieldType, penum, &bufferSize);
    }

    // The first call can fail with ERROR_NOT_FOUND if none of the provider's event
    // descriptions contain the requested field type information.

    if (ERROR_SUCCESS == status)
    {
        // Loop through the list of field information and print the field's name,
        // description (if it exists), and value. 

        for (DWORD i = 0; i < penum->NumberOfElements; i++)
        {
            wprintf(L"Field name: %s\nDescription: %s\nValue: %I64u\n\n",
                (PWCHAR)((PBYTE)(penum) + penum->FieldInfoArray[i].NameOffset),
                (penum->FieldInfoArray[i].DescriptionOffset) ? 
                    (PWCHAR)((PBYTE)(penum) + penum->FieldInfoArray[i].DescriptionOffset): L"",
                penum->FieldInfoArray[i].Value);
        }
    }
    else
    {
        if (ERROR_NOT_FOUND == status)
        {
            wprintf(L"Requested field type not found.\n");
        }
        else
        {
            wprintf(L"TdhEnumerateProviderFieldInformation failed with %lu.\n", status);
        }

        goto cleanup;
    }

cleanup:

    if (penum)
    {
        free(penum);
        penum = NULL;
    }

    return status;
}

```

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviders">TdhEnumerateProviders</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhqueryproviderfieldinformation">TdhQueryProviderFieldInformation</a>