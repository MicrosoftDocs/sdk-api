---
UID: NC:winbio_adapter.PIBIO_STORAGE_CONTROL_UNIT_PRIVILEGED_FN
title: PIBIO_STORAGE_CONTROL_UNIT_PRIVILEGED_FN
author: windows-sdk-content
description: Performs a vendor-defined control operation that requires elevated privilege.
old-location: secbiomet\storageadaptercontrolunitprivileged.htm
old-project: SecBioMet
ms.assetid: 42e33817-df5f-4598-bc6a-94e49ce5fca4
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PIBIO_STORAGE_CONTROL_UNIT_PRIVILEGED_FN, PIBIO_STORAGE_CONTROL_UNIT_PRIVILEGED_FN callback, StorageAdapterControlUnitPrivileged, StorageAdapterControlUnitPrivileged callback function [Windows Biometric Framework API], secbiomet.storageadaptercontrolunitprivileged, winbio_adapter/StorageAdapterControlUnitPrivileged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - StorageAdapterControlUnitPrivileged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_CONTROL_UNIT_PRIVILEGED_FN callback function


## -description


Called by the Windows Biometric Framework to perform a vendor-defined control operation that requires elevated privilege. Call the <a href="https://msdn.microsoft.com/98981278-9d30-4e7d-a9b6-d0427ed8b385">StorageAdapterControlUnit</a> function to perform a vendor-defined control operation that does not require elevated privilege.


## -parameters




### -param Pipeline [in, out]

A pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param ControlCode [in]

A <b>ULONG</b> value that specifies the vendor-defined operation to perform.


### -param SendBuffer [in]

A pointer to a buffer that contains the control information sent to the storage adapter. The format and content of the buffer is vendor defined.


### -param SendBufferSize [in]

The size, in bytes, of the buffer specified by the <i>SendBuffer</i> parameter.


### -param ReceiveBuffer [in]

A pointer to a buffer that receives information returned by the storage adapter in response to the control operation. The format of the buffer is vendor defined.


### -param ReceiveBufferSize [in]

The size, in bytes, of the buffer specified by the <i>ReceiveBuffer</i> parameter.


### -param ReceiveDataSize [out]

A pointer to a variable that receives  the size, in bytes, of the data written to the buffer specified by the <i>ReceiveBuffer</i> parameter.


### -param OperationStatus [out]

A pointer to a variable that receives a vendor-defined status code that specifies the outcome of the control operation.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

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



Your implementation of this function should be identical to your implementation of the <a href="https://msdn.microsoft.com/98981278-9d30-4e7d-a9b6-d0427ed8b385">StorageAdapterControlUnit</a> function except that elevated privileges are required to perform the operations specified by the <i>ControlCode</i> parameter. You are responsible for defining the operations and deciding which will require elevated privilege.

This function must check the value of the <i>ReceiveBufferSize</i> parameter to be certain that the buffer specified by the <i>ReceiveBuffer</i> parameter is large enough to hold the data being returned.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterControlUnitPrivileged
//
// Purpose:
//      Performs a vendor-defined control operation that requires elevated privilege.
//
// Parameters:
//      Pipeline            - Pointer to a WINBIO_PIPELINE structure associated 
//                            with the biometric unit performing the operation
//      ControlCode         - Specifies the vendor-defined operation to perform
//      SendBuffer          - Contains the control information sent to the 
//                            storage adapter
//      SendBufferSize      - Size, in bytes, of the buffer specified by the 
//                            SendBuffer parameter
//      ReceiveBuffer       - Receives information returned by the storage adapter
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
StorageAdapterControlUnitPrivileged(
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
    PWINBIO_STORAGE_CONTEXT storageContext = 
           (PWINBIO_STORAGE_CONTEXT)Pipeline-&gt;StorageContext;

    // Verify the state of the pipeline.
    if (storageContext == NULL ||
        Pipeline-&gt;StorageHandle == INVALID_HANDLE_VALUE)
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
            if (SendBufferSize &lt; sizeof(CTRL_CODE_P1_SEND_BUFFER))
            {
                hr = E_INVALIDARG;
                break;
            }

            // Perform any other checks that may be required on the buffer 
            // contents. Return E_INVALIDARG if any of the checks fail.
            if (sendBuffer-&gt;SomeField != SomeSpecialValue ||
                sendBuffer-&gt;SomeOtherField != SomeOtherSpecialValue)
            {
                hr = E_INVALIDARG;
                break;
            }

            if (ReceiveBufferSize &lt; sizeof(CTRL_CODE_P1_RECEIVE_BUFFER))
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
        // Continue testing for other non-privileged control codes that your
        // adapter supports.
        {
            CTRL_CODE_P2_SEND_BUFFER *sendBuffer = (CTRL_CODE_P2_SEND_BUFFER*)SendBuffer;

            // Verify the size of the send buffer.
            if (SendBufferSize &lt; sizeof(CTRL_CODE_P2_SEND_BUFFER))
            {
                hr = E_INVALIDARG;
                break;
            }

            // Perform any other checks that may be required on the buffer 
            // contents. Return E_INVALIDARG if any of the checks fail.
            if (sendBuffer-&gt;SomeField != SomeSpecialValue ||
                sendBuffer-&gt;SomeOtherField != SomeOtherSpecialValue)
            {
                hr = E_INVALIDARG;
                break;
            }

            if (ReceiveBufferSize &lt; sizeof(CTRL_CODE_P2_RECEIVE_BUFFER))
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
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // If control code validation succeeds, perform the control operation. This
    // example assumes that your adapter has put an open handle to a storage 
    // device in the Pipeline structure. It also assumes that the driver performs
    // overlapped I/O and that a properly initialized OVERLAPPED structure is
    // contained in the storage context.
    result = DeviceIoControl(
                Pipeline-&gt;StorageHandle,
                ControlCode,
                SendBuffer,
                (DWORD)SendBufferSize,
                ReceiveBuffer,
                (DWORD)ReceiveBufferSize,
                (LPDWORD)ReceiveDataSize,
                &amp;storageContext-&gt;Overlapped
                );
    if (result == FALSE &amp;&amp; GetLastError() == ERROR_IO_PENDING)
    {
        SetLastError(ERROR_SUCCESS);

        result = GetOverlappedResult(
                    Pipeline-&gt;StorageHandle,
                    &amp;storageContext-&gt;Overlapped,
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/98981278-9d30-4e7d-a9b6-d0427ed8b385">StorageAdapterControlUnit</a>
 

 

