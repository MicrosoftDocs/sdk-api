---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN
title: PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN (winbio_adapter.h)
description: Retrieves the size of the index vector used by the engine adapter.
helpviewer_keywords: ["EngineAdapterQueryIndexVectorSize","EngineAdapterQueryIndexVectorSize callback function [Windows Biometric Framework API]","PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN","PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN callback","secbiomet.engineadapterqueryindexvectorsize","winbio_adapter/EngineAdapterQueryIndexVectorSize"]
old-location: secbiomet\engineadapterqueryindexvectorsize.htm
tech.root: SecBioMet
ms.assetid: 07e9f956-1bae-4011-92a0-6c5ed0d105a0
ms.date: 12/05/2018
ms.keywords: EngineAdapterQueryIndexVectorSize, EngineAdapterQueryIndexVectorSize callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN, PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN callback, secbiomet.engineadapterqueryindexvectorsize, winbio_adapter/EngineAdapterQueryIndexVectorSize
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN
 - winbio_adapter/PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQueryIndexVectorSize
---

# PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN callback function


## -description

Called by the Windows Biometric Framework  to retrieve the size of the index vector used by the engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param IndexElementCount [out]

Address of a variable that receives the number of array elements in the index vector.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The index vector is used by the engine adapter to index the available biometric templates.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
///////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterQueryIndexVectorSize
//
// Purpose:
//      Called by the Windows Biometric Framework to retrieve the size of 
//      the index vector used by the engine adapter.
//
// Parameters:
//      Pipeline            - Pointer to a WINBIO_PIPELINE structure associated 
//                            with the biometric unit performing the operation.
//      IndexElementCount   - Address of a variable that receives the number of 
//                            elements in the index vector.
//
static HRESULT
WINAPI
EngineAdapterQueryIndexVectorSize(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PSIZE_T IndexElementCount
    )
{
    HRESULT hr = S_OK;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(IndexElementCount))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Specify the number of index vector elements supported by your adapter. This can
    // be any positive value or zero. Return zero if your adapter does not support placing 
    // templates into buckets. That is, return zero if your adapter does not support index 
    // vectors.
    *IndexElementCount = NUMBER_OF_TEMPLATE_BINS;

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>