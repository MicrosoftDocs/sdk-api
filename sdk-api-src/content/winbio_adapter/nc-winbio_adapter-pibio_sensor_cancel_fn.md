---
UID: NC:winbio_adapter.PIBIO_SENSOR_CANCEL_FN
title: PIBIO_SENSOR_CANCEL_FN (winbio_adapter.h)
description: Cancels all pending sensor operations.
helpviewer_keywords: ["PIBIO_SENSOR_CANCEL_FN","PIBIO_SENSOR_CANCEL_FN callback","SensorAdapterCancel","SensorAdapterCancel callback function [Windows Biometric Framework API]","secbiomet.sensoradaptercancel","winbio_adapter/SensorAdapterCancel"]
old-location: secbiomet\sensoradaptercancel.htm
tech.root: SecBioMet
ms.assetid: 11a0728e-1833-43b3-8ae2-0393743bb19b
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_CANCEL_FN, PIBIO_SENSOR_CANCEL_FN callback, SensorAdapterCancel, SensorAdapterCancel callback function [Windows Biometric Framework API], secbiomet.sensoradaptercancel, winbio_adapter/SensorAdapterCancel
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
 - PIBIO_SENSOR_CANCEL_FN
 - winbio_adapter/PIBIO_SENSOR_CANCEL_FN
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
 - SensorAdapterCancel
---

# PIBIO_SENSOR_CANCEL_FN callback function


## -description

Called by the Windows Biometric Framework to cancel all pending sensor operations.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
The <i>Pipeline</i> argument cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorHandle</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
</table>

## -remarks

Your implementation of this function should not wait for pending operations to complete.

If the sensor has no pending operations when this function is called, your implementation must return S_OK without changing the state of the pipeline.



#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterCancel
//
// Purpose:
//      Cancels all pending sensor operations.
//      
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit.
//
static HRESULT
WINAPI
SensorAdapterCancel(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    HRESULT hr = S_OK;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Validate the current sensor state.
    if (Pipeline->SensorHandle == INVALID_HANDLE_VALUE)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Cancel all I/O to the sensor handle.
    if (!CancelIoEx(Pipeline->SensorHandle, NULL))
    {
        hr = _SensorAdapterGetHresultFromWin32(GetLastError());
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>