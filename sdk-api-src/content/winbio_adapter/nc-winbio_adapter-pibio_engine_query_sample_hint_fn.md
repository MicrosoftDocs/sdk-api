---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN
title: PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN
author: windows-sdk-content
description: Retrieves the number of correct samples required by the engine adapter to construct an enrollment template.
old-location: secbiomet\engineadapterquerysamplehint.htm
old-project: secbiomet
ms.assetid: 9208cd3e-205d-4ef0-8f67-292385dea9a2
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EngineAdapterQuerySampleHint, EngineAdapterQuerySampleHint callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN, PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN callback, secbiomet.engineadapterquerysamplehint, winbio_adapter/EngineAdapterQuerySampleHint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.redist: 
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQuerySampleHint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN callback function


## -description


Called by the Windows Biometric Framework to retrieve the number of correct samples required by the engine adapter to construct an enrollment template.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param SampleHint [out]

Pointer to a variable that receives the number of required samples.


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
<dt><b>WINBIO_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support this property.

</td>
</tr>
</table>
 




## -remarks



If an engine adapter requires a different number of samples in different situations, you should return the largest number. For example, if a fingerprint engine requires more swipes for an index finger than for a thumb, return the number required for the index finger.

The value returned by the <i>SampleHint</i> parameter specifies the number of correct samples required. Because of bad captures, the actual number of samples required during enrollment may be larger than the number specified.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterQuerySampleHint
//
// Purpose: 
//      Retrieves the number of correct samples required by the engine adapter 
//      to construct an enrollment template.
//
// Parameters:
//      Pipeline    - Pointer to a WINBIO_PIPELINE structure associated 
//                    with the biometric unit performing the operation. 
//      SampleHint  - Pointer to a variable that receives the number of 
//                    required samples.
//
static HRESULT
WINAPI
EngineAdapterQuerySampleHint(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PSIZE_T SampleHint
    )
{
    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(SampleHint))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // The sample hint specified here is a constant but can also be a 
    // function of the hardware model or the device settings depending
    // on your adapter.
    // If your adapter does not support this feature, return
    // WINBIO_E_UNSUPPORTED_PROPERTY.
    *SampleHint = SAMPLES_REQUIRED_FOR_ENROLLMENT;

cleanup:

    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/fa6c5aa4-a9f4-421e-bc43-ced7fade4144">EngineAdapterAcceptSampleData</a>



<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

