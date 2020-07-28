---
UID: NC:winbio_adapter.PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN
title: PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN (winbio_adapter.h)
description: Performs a vendor-defined control operation that requires elevated privilege.
helpviewer_keywords: ["EngineAdapterControlUnitPrivileged","EngineAdapterControlUnitPrivileged callback function [Windows Biometric Framework API]","PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN","PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN callback","secbiomet.engineadaptercontrolunitprivileged","winbio_adapter/EngineAdapterControlUnitPrivileged"]
old-location: secbiomet\engineadaptercontrolunitprivileged.htm
tech.root: SecBioMet
ms.assetid: 1d1fda45-3822-40c0-ac84-0fcdef1a6498
ms.date: 12/05/2018
ms.keywords: EngineAdapterControlUnitPrivileged, EngineAdapterControlUnitPrivileged callback function [Windows Biometric Framework API], PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN, PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN callback, secbiomet.engineadaptercontrolunitprivileged, winbio_adapter/EngineAdapterControlUnitPrivileged
f1_keywords:
- winbio_adapter/EngineAdapterControlUnitPrivileged
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- EngineAdapterControlUnitPrivileged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN callback function


## -description


Called by the Windows Biometric Framework to perform a vendor-defined control operation that requires elevated privilege. Call the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn">EngineAdapterControlUnit</a> function to perform a vendor-defined control operation that does not require elevated privilege.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.



### -param ControlCode [in]

A <b>ULONG</b> value that specifies the vendor-defined operation to perform.


### -param SendBuffer [in]

Pointer to a buffer that contains the control information sent to the engine adapter. The format and content of the buffer is vendor-defined.


### -param SendBufferSize [in]

Size, in bytes, of the buffer specified by the <i>SendBuffer</i> parameter.


### -param ReceiveBuffer [in]

Pointer to a  buffer that receives information returned by the engine adapter in response to the control operation.  The format of the buffer is vendor-defined.


### -param ReceiveBufferSize [in]

Size, in bytes, of the buffer specified by the <i>ReceiveBuffer</i> parameter.


### -param ReceiveDataSize [out]

Pointer to a variable that receives the size, in bytes, of the data written to the buffer specified by the <i>ReceiveBuffer</i> parameter.


### -param OperationStatus [out]

Pointer to a variable that receives a vendor-defined status code that specifies the outcome of the control operation.


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
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b> E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
The size or format of the buffer specified by the <i>SendBuffer</i> parameter is not correct, or the value specified in the <i>ControlCode</i> parameter is not recognized by the adapter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by the <i>ReceiveBuffer</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
There was a hardware failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_INVALID_CONTROL_CODE</b></b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>ControlCode</i> parameter is not recognized by the adapter.

<div class="alert"><b>Note</b>  Beginning with Windows 8, use only <b>E_INVALIDARG</b> to signal this condition.</div>
<div> </div>
</td>
</tr>
</table>
 




## -remarks



Your implementation of this function should be identical to your implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn">EngineAdapterControlUnit</a> function except that elevated privileges are required to perform the operations specified by the <i>ControlCode</i> parameter. You are responsible for defining the operations and deciding which will require elevated privilege.

This function must check the value of the <i>ReceiveBufferSize</i> parameter to be certain that the buffer specified by the <i>ReceiveBuffer</i> parameter is large enough to hold the data being returned.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
///////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterControlUnitPrivileged
//
// Purpose:
//      Performs a vendor-defined control operation that requires elevated 
//      privilege.
//
// Parameters:
//      Pipeline            - Pointer to a WINBIO_PIPELINE structure associated 
//                            with the biometric unit performing the operation
//      ControlCode         - Specifies the vendor-defined operation to perform
//      SendBuffer          - Contains the control information sent to the 
//                            engine adapter
//      SendBufferSize      - Size, in bytes, of the buffer specified by the 
//                            SendBuffer parameter
//      ReceiveBuffer       - Receives information returned by the engine adapter
//                            in response to the control operation
//      ReceiveBufferSize   - Size, in bytes, of the buffer specified by the 
//                            ReceiveBuffer parameter.
//      ReceiveDataSize     - Receives the size, in bytes, of the data written to 
//                            the buffer specified by the ReceiveBuffer parameter
//      OperationStatus     - Receives a vendor-defined status code that specifies 
//                            the outcome of the control operation.
//
static HRESULT
WINAPI
EngineAdapterControlUnitPrivileged(
    __inout PWINBIO_PIPELINE Pipeline,
    __in ULONG ControlCode,
    __in PUCHAR SendBuffer,
    __in SIZE_T SendBufferSize,
    __in PUCHAR ReceiveBuffer,
    __in SIZE_T ReceiveBufferSize,
    __out PSIZE_T ReceiveDataSize,
    __out PULONG OperationStatus
    )
{
    HRESULT hr = S_OK;
    BOOL result = TRUE;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(SendBuffer) ||
        !ARGUMENT_PRESENT(ReceiveBuffer) ||
        !ARGUMENT_PRESENT(ReceiveDataSize) ||
        !ARGUMENT_PRESENT(OperationStatus))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT engineContext = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // Verify the state of the pipeline.
    if (engineContext == NULL ||
        engineContext->FileHandle == INVALID_HANDLE_VALUE)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    switch (ControlCode)
    {
    case MY_PRIVILEGED_CTRL_CODE_P1:
        {
            CTRL_CODE_P1_SEND_BUFFER *sendBuffer = (CTRL_CODE_P1_SEND_BUFFER*)SendBuffer;

            // Verify the size of the send buffer.
            if (SendBufferSize < sizeof(CTRL_CODE_P1_SEND_BUFFER))
            {
                hr = E_INVALIDARG;
                break;
            }

            // Perform any other checks that may be required on the buffer 
            // contents. Return E_INVALIDARG if any of the checks fail.
            if (sendBuffer->SomeField != SomeSpecialValue ||
                sendBuffer->SomeOtherField != SomeOtherSpecialValue)
            {
                hr = E_INVALIDARG;
                break;
            }

            if (ReceiveBufferSize < sizeof(CTRL_CODE_P1_RECEIVE_BUFFER))
            {
                hr = E_NOT_SUFFICIENT_BUFFER;
                break;
            }
        }

        // Fall through and perform the control operation after the switch
        // statement. Alternatively, depending on your requirements, you can 
        // perform the control operation here.
        break;

    case MY_PRIVILEGED_CTRL_CODE_P2:
        // Continue testing for other privileged control codes that your
        // adapter supports.
        {
            CTRL_CODE_P2_SEND_BUFFER *sendBuffer = (CTRL_CODE_P2_SEND_BUFFER*)SendBuffer;

            // Verify the size of the send buffer.
            if (SendBufferSize < sizeof(CTRL_CODE_P2_SEND_BUFFER))
            {
                hr = E_INVALIDARG;
                break;
            }

            // Perform any other checks that may be required on the buffer 
            // contents. Return E_INVALIDARG if any of the checks fail.
            if (sendBuffer->SomeField != SomeSpecialValue ||
                sendBuffer->SomeOtherField != SomeOtherSpecialValue)
            {
                hr = E_INVALIDARG;
                break;
            }

            if (ReceiveBufferSize < sizeof(CTRL_CODE_P2_RECEIVE_BUFFER))
            {
                hr = E_NOT_SUFFICIENT_BUFFER;
                break;
            }
        }
        break;

    default:
        // All unrecognized control code values should return an error.
        hr = WINBIO_E_INVALID_CONTROL_CODE;
        break;
    }

    // If control code validation succeeds, perform the control operation. This
    // example assumes that your adapter context structure contains an open
    // handle to a hardware driver. It also assumes that the driver performs
    // overlapped I/O and that a properly initialized OVERLAPPED structure is
    // contained in the engine context.
    if (FAILED(hr))
    {
        goto cleanup;
    }
    result = DeviceIoControl(
                Pipeline->EngineHandle,
                ControlCode,
                SendBuffer,
                (DWORD)SendBufferSize,
                ReceiveBuffer,
                (DWORD)ReceiveBufferSize,
                (LPDWORD)ReceiveDataSize,
                &Pipeline->EngineContext->Overlapped
                );
    if (result == FALSE && GetLastError() == ERROR_IO_PENDING)
    {
        SetLastError(ERROR_SUCCESS);

        result = GetOverlappedResult(
                    Pipeline->EngineHandle,
                    &Pipeline->EngineContext->Overlapped,
                    (LPDWORD)ReceiveDataSize,
                    TRUE
                    );
    }
    *OperationStatus = GetLastError();

    if (!result)
    {
        hr = _AdapterGetHresultFromWin32(*OperationStatus);
    }

cleanup:

    return hr;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn">EngineAdapterControlUnit</a>



<a href="https://docs.microsoft.com/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>
 

 

