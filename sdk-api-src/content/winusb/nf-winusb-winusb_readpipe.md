---
UID: NF:winusb.WinUsb_ReadPipe
title: WinUsb_ReadPipe function (winusb.h)
description: The WinUsb_ReadPipe function reads data from the specified pipe.
helpviewer_keywords: ["WinUsb_ReadPipe","WinUsb_ReadPipe function [Buses]","buses.winusb_readpipe","winusb/WinUsb_ReadPipe","winusbfunc_a18a80b3-9f2b-45a5-bd34-dac4bddb1053.xml"]
old-location: buses\winusb_readpipe.htm
tech.root: buses
ms.assetid: 936e535b-9084-4e3d-908e-0e965f658827
ms.date: 12/05/2018
ms.keywords: WinUsb_ReadPipe, WinUsb_ReadPipe function [Buses], buses.winusb_readpipe, winusb/WinUsb_ReadPipe, winusbfunc_a18a80b3-9f2b-45a5-bd34-dac4bddb1053.xml
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_ReadPipe
 - winusb/WinUsb_ReadPipe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_ReadPipe
---

# WinUsb_ReadPipe function


## -description

The <b>WinUsb_ReadPipe</b> function reads data from the specified pipe.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the interface that contains the endpoint with which the pipe is associated. 

To read data from the pipe associated with an endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

<i>PipeID</i> corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor. For information about the layout of this field, see <b>Table 9-13</b> in "Universal Serial Bus Specification Revision 2.0" at <a href="https://www.microsoft.com/whdc/connect/usb/default.mspx">USB Technology</a>. In the <b>bEndpointAddress</b> field, Bit 7 indicates the direction of the endpoint: 0 for OUT; 1 for IN.

### -param Buffer [out]

A caller-allocated buffer that receives the data that is read.

### -param BufferLength [in]

The maximum number of bytes to read. This number must be less than or equal to the size, in bytes, of <i>Buffer</i>.

### -param LengthTransferred [out, optional]

A pointer to a ULONG variable that receives the actual number of bytes that were copied into <i>Buffer</i>. For more information, see Remarks.

### -param Overlapped [in, optional]

An optional pointer to an OVERLAPPED structure that is used for asynchronous operations. If this parameter is specified, <b>WinUsb_ReadPipe</b> returns immediately rather than waiting synchronously for the operation to complete before returning. An event is signaled when the operation is complete.

## -returns

<b>WinUsb_ReadPipe</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


<b>GetLastError</b>    can return the following error code.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
An overlapped I/O operation is in progress but has not completed.  If the overlapped operation cannot be completed immediately, the function returns <b>FALSE</b> and the <b>GetLastError</b> function returns ERROR_IO_PENDING, indicating that the operation is executing in the background. Call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getoverlappedresult">WinUsb_GetOverlappedResult</a> to check the success or failure of the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The read operation initiated by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_readpipe">WinUsb_ReadPipe</a>  in the USB stack timed out before the operation could be completed.

</td>
</tr>
</table>

## -remarks

If the data returned by the device is greater than a maximum transfer length, WinUSB divides the request into smaller requests of maximum transfer length and submits them serially. If the transfer length is not a multiple of the endpoint's maximum packet size (retrievable through  the <a href="/windows/desktop/api/winusbio/ns-winusbio-winusb_pipe_information">WINUSB_PIPE_INFORMATION</a> structure's <b>MaximumPacketSize</b> member), WinUSB increases the size of the transfer to the next multiple of <b>MaximumPacketSize</b>.

USB packet size does not factor into the transfer for a read request. If the device responds with a packet that is too large for the client buffer, the behavior of the read request corresponds to the type of policy set on the pipe. If policy type for the pipe is ALLOW_PARTIAL_READS, WinUSB adds the remaining data to the beginning of the next transfer. If ALLOW_PARTIAL_READS is not set, the read request fails. For more information about policy types, see <a href="/windows-hardware/drivers/ddi/content/index">WinUSB Functions for Pipe Policy Modification</a>.

If an application passes <b>NULL</b> in the <i>Overlapped</i> parameter (synchronous operation), the application must make sure that <i>LengthTransferred</i> is not <b>NULL</b>, even when the read  operation produces no output data.

If <i>Overlapped</i> is not <b>NULL</b> (asynchronous operation),  <i>LengthTransferred</i> can be set to <b>NULL</b>. For an overlapped operation (and if <i>LengthTransferred</i> is a non-<b>NULL</b> value), the value received in <i>LengthTransferred</i> after <b>WinUsb_ReadPipe</b> returns is meaningless until the overlapped operation has completed. To retrieve the actual number of bytes read from the pipe, call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getoverlappedresult">WinUsb_GetOverlappedResult</a>.

When no data is available in the endpoint (pipe is empty), <b>WinUsb_ReadPipe</b> does not return until there is data in the pipe. If an error condition occurs or the application-specified timeout expires,   <b>WinUsb_ReadPipe</b> always returns FALSE. To determine the actual reason for that return value, always call <b>GetLastError</b>. For example, in these cases the <b>GetLastError</b> error value indicates the actual reason: <ul>
<li>If the application specified a timeout value in the pipe policy and that timeout expires, <b>WinUsb_ReadPipe</b> returns  FALSE and <b>GetLastError</b> returns ERROR_SEM_TIMEOUT.</li>
<li>If an error condition occurs while reading data from the pipe, <b>WinUsb_ReadPipe</b> returns FALSE and <b>GetLastError</b> returns ERROR_GEN_FAILURE.</li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>