---
UID: NC:winbio_adapter.PIBIO_ENGINE_SET_HASH_ALGORITHM_FN
title: PIBIO_ENGINE_SET_HASH_ALGORITHM_FN (winbio_adapter.h)
description: Selects a hash algorithm for use in subsequent operations.
helpviewer_keywords: ["EngineAdapterSetHashAlgorithm","EngineAdapterSetHashAlgorithm callback function [Windows Biometric Framework API]","PIBIO_ENGINE_SET_HASH_ALGORITHM_FN","PIBIO_ENGINE_SET_HASH_ALGORITHM_FN callback","secbiomet.engineadaptersethashalgorithm","winbio_adapter/EngineAdapterSetHashAlgorithm"]
old-location: secbiomet\engineadaptersethashalgorithm.htm
tech.root: SecBioMet
ms.assetid: 0d16d82a-287c-4402-ac10-f601684bd976
ms.date: 12/05/2018
ms.keywords: EngineAdapterSetHashAlgorithm, EngineAdapterSetHashAlgorithm callback function [Windows Biometric Framework API], PIBIO_ENGINE_SET_HASH_ALGORITHM_FN, PIBIO_ENGINE_SET_HASH_ALGORITHM_FN callback, secbiomet.engineadaptersethashalgorithm, winbio_adapter/EngineAdapterSetHashAlgorithm
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
 - PIBIO_ENGINE_SET_HASH_ALGORITHM_FN
 - winbio_adapter/PIBIO_ENGINE_SET_HASH_ALGORITHM_FN
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
 - EngineAdapterSetHashAlgorithm
---

# PIBIO_ENGINE_SET_HASH_ALGORITHM_FN callback function


## -description

Called by the Windows Biometric Framework to select a hash algorithm for use in subsequent operations.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param AlgorithmBufferSize [in]

The size, in bytes, of the buffer specified by the <i>AlgorithmBuffer</i> parameter.

### -param AlgorithmBuffer [in]

Pointer to a <b>NULL</b>-terminated ANSI string that contains the object identifier of the hash algorithm to select. Call the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn">EngineAdapterQueryHashAlgorithms</a> function to retrieve an array of the supported algorithm object identifiers (OIDs).

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support template hashing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support the hash algorithm specified by the <i>AlgorithmBuffer</i> parameter.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function to configure a biometric unit every time the unit is added to a sensor pool.

 Because a hash algorithm is selected on a per-pipeline basis, the engine adapter must store the selected algorithm in a private pipeline context.

The engine adapter must keep track of the most recent algorithm selected and use this algorithm when processing calls to the following functions:

<ul>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn">EngineAdapterVerifyFeatureSet</a>
</li>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn">EngineAdapterIdentifyFeatureSet</a>
</li>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn">EngineAdapterGetEnrollmentHash</a>
</li>
</ul>
The algorithm chosen by this function must remain selected until the next time <i>EngineAdapterSetHashAlgorithm</i> is called, or until the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn">EngineAdapterDetach</a> method is called. In particular, calls to the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn">EngineAdapterClearContext</a> function should not affect the selected algorithm.

Only the SHA1 hash algorithm is used by the Windows Biometric Framework. The OID string value for this algorithm is "1.3.14.3.2.26". For more information, see <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn">EngineAdapterQueryHashAlgorithms</a>.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterSetHashAlgorithm
//
// Purpose:
//      Selects a hash algorithm for use in subsequent operations.
//
// Parameters:
//      Pipeline            - Pointer to a WINBIO_PIPELINE structure associated 
//                            with the biometric unit performing the operation.   
//      AlgorithmBufferSize - Size, in bytes, of the buffer specified by the 
//                            AlgorithmBuffer parameter.
//      AlgorithmBuffer     - Pointer to a NULL-terminated ANSI string that 
//                            contains the object identifier of the hash algorithm
//                            to select.
//
static HRESULT
WINAPI
EngineAdapterSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    ////////////////////////////////////////////////////////////////////////////
    // Return E_NOTIMPL here if your adapter does not support template hashing.
    ////////////////////////////////////////////////////////////////////////////

    HRESULT hr = S_OK;
    SIZE_T algorithmSize = (strlen(szOID_OIWSEC_sha1) + 1) * sizeof(CHAR);

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(AlgorithmBuffer))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Only the SHA1 hashing algorithm is supported.
    // Therefore, make certain that SHA1 is included in the algorithm
    // table.
    // The SHA1 object identifier, szOID_OIWSEC_sha1, is contained in the
    // Wincrypt.h header file.
    if (AlgorithmBufferSize != algorithmSize ||
        memcmp(AlgorithmBuffer, szOID_OIWSEC_sha1, algorithmSize) != 0)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Make any necessary changes to the adapter state to specify that
    // SHA1 hashing is enabled. If your adapter does not support template
    // hashing, return E_NOTIMPL.

cleanup:
    
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn">EngineAdapterQueryHashAlgorithms</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>