---
UID: NC:winbio_adapter.PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN
title: PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN (winbio_adapter.h)
description: Retrieves a copy of the most recently processed feature set or template from the engine in a standard biometric information record.
helpviewer_keywords: ["EngineAdapterExportEngineData","EngineAdapterExportEngineData callback function [Windows Biometric Framework API]","PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN","PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN callback","WINBIO_DATA_FLAG_INTEGRITY","WINBIO_DATA_FLAG_INTERMEDIATE","WINBIO_DATA_FLAG_PRIVACY","WINBIO_DATA_FLAG_PROCESSED","WINBIO_DATA_FLAG_RAW","WINBIO_DATA_FLAG_SIGNED","secbiomet.engineadapterexportenginedata","winbio_adapter/EngineAdapterExportEngineData"]
old-location: secbiomet\engineadapterexportenginedata.htm
tech.root: SecBioMet
ms.assetid: 9ac11720-7dbf-4479-b2c5-78cd53494e21
ms.date: 11/19/2020
ms.keywords: EngineAdapterExportEngineData, EngineAdapterExportEngineData callback function [Windows Biometric Framework API], PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN, PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN callback, WINBIO_DATA_FLAG_INTEGRITY, WINBIO_DATA_FLAG_INTERMEDIATE, WINBIO_DATA_FLAG_PRIVACY, WINBIO_DATA_FLAG_PROCESSED, WINBIO_DATA_FLAG_RAW, WINBIO_DATA_FLAG_SIGNED, secbiomet.engineadapterexportenginedata, winbio_adapter/EngineAdapterExportEngineData
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
 - PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN
 - winbio_adapter/PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN
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
 - EngineAdapterExportEngineData
---

# PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN callback function


## -description

Called by the Windows Biometric Framework to retrieve a copy of the most recently processed feature set or template from the engine formatted as a standard <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Flags [in]

A value that specifies the properties of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned by the engine. This can be a bitwise <b>OR</b> of the following security and processing level flags:


 **WINBIO_DATA_FLAG_PRIVACY**

The data is encrypted.
            
            
* **WINBIO_DATA_FLAG_INTEGRITY**
The data is digitally signed or protected by a message authentication code (MAC).
            
            
* **WINBIO_DATA_FLAG_SIGNED**
If this flag and the <mark>WINBIO_DATA_FLAG_INTEGRITY</mark> flag are set, the data is signed. If this flag is not set but the <mark>WINBIO_DATA_FLAG_INTEGRITY</mark> flag is set, a MAC is computed.
            
            
* **WINBIO_DATA_FLAG_RAW**
The data is in the format with which it was captured.
            
            
* **WINBIO_DATA_FLAG_INTERMEDIATE**
The data is not raw but has not been completely processed.
            
            
* **WINBIO_DATA_FLAG_PROCESSED**
The data has been processed.

### -param SampleBuffer [out]

Address of a variable that receives a pointer to a <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that contains the feature set or template.

### -param SampleSize [out]

Pointer to a variable that contains the size, in bytes, of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned in the <i>SampleBuffer</i> parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support the combination of flags specified by the  <i>Flags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to create the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure.

</td>
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
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pipeline does not contain the type of data required by the <i>Flags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not currently implemented.

</td>
</tr>
</table>

## -remarks

You must allocate the buffer to be returned in the <i>SampleBuffer</i> parameter from the process heap by using the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function. After the buffer is created, it becomes the property of the Windows Biometric Framework. Because the Framework deallocates this memory when finished using it, your implementation of this function  must not attempt to deallocate the buffer or save a pointer to it.  By not saving the pointer, you prevent other parts of the engine adapter from attempting to use the buffer after this function returns.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterExportEngineData
//
// Purpose:
//      Retrieves a copy of the most recently processed feature set or template.
//
// Parameters:
//      Pipeline        - Pointer to a WINBIO_PIPELINE structure associated 
//                        with the biometric unit performing the operation
//      Flags           - Security and processing level flags
//      SampleBuffer    - Contains the feature set or template
//      SampleSize      - Size, in bytes, of the structure returned in the 
//                        SampleBuffer parameter.
//
static HRESULT
WINAPI
EngineAdapterExportEngineData(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_DATA_FLAGS Flags,
    __out PWINBIO_BIR *SampleBuffer,
    __out PSIZE_T SampleSize
    )
{
    HRESULT hr = S_OK;
    PWINBIO_BIR birAddress = NULL;
    SIZE_T birSize = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(SampleBuffer) ||
        !ARGUMENT_PRESENT(SampleSize))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // At least one processing level flag must be set. Your adapter can also
    // place additional restrictions on supported export formats.
    if (Flags & (WINBIO_DATA_FLAG_RAW | 
                 WINBIO_DATA_FLAG_INTERMEDIATE | 
                 WINBIO_DATA_FLAG_PROCESSED) == 0)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // You must implement the _CreateBirFromAdapterData function to extract
    // data from the engine context and create a new WINBIO_BIR structure. The
    // function passes ownership of the new biometric information record (BIR)
    // to the EngineAdapterExportEngineData routine which then passes the BIR
    // to the caller.
    hr = _CreateBirFromAdapterData( context, Flags, &birAddress, &birSize);
    if (SUCCEEDED(hr))
    {
        *SampleBuffer = birAddress;
        *SampleSize = birSize;
    }

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn">EngineAdapterAcceptSampleData</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>
