---
UID: NF:winusb.WinUsb_WritePipe
title: WinUsb_WritePipe function (winusb.h)
description: The WinUsb_WritePipe function writes data to a pipe.
helpviewer_keywords: ["WinUsb_WritePipe","WinUsb_WritePipe function [Buses]","buses.winusb_writepipe","winusb/WinUsb_WritePipe","winusbfunc_6fbed2b9-a65e-4802-8ba4-369a3200bffd.xml"]
old-location: buses\winusb_writepipe.htm
tech.root: buses
ms.assetid: 995b1d1b-8c08-4e67-8ba5-155231fe37f4
ms.date: 12/05/2018
ms.keywords: WinUsb_WritePipe, WinUsb_WritePipe function [Buses], buses.winusb_writepipe, winusb/WinUsb_WritePipe, winusbfunc_6fbed2b9-a65e-4802-8ba4-369a3200bffd.xml
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
 - WinUsb_WritePipe
 - winusb/WinUsb_WritePipe
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
 - WinUsb_WritePipe
---

# WinUsb_WritePipe function


## -description

The <b>WinUsb_WritePipe</b> function writes data to a pipe.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the interface that contains the endpoint with which the pipe is associated. 

To write to  a pipe that is associated with an endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

<i>PipeID</i> corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor. For information about the layout of this field, see <b>Table 9-13</b> in "Universal Serial Bus Specification Revision 2.0" at <a href="https://www.microsoft.com/whdc/connect/usb/default.mspx">USB Technology</a>. In the <b>bEndpointAddress</b> field, Bit 7 indicates the direction of the endpoint: 0 for OUT; 1 for IN.

### -param Buffer [in]

A caller-allocated buffer that contains the data to write.

### -param BufferLength [in]

The number of bytes to write. This number must be less than or equal to the size, in bytes, of <i>Buffer</i>.

### -param LengthTransferred [out, optional]

A pointer to a ULONG variable that receives the actual number of bytes that were written to the pipe. For more information, see Remarks.

### -param Overlapped [in, optional]

An optional pointer to an OVERLAPPED structure, which is used for asynchronous operations. If this parameter is specified, <b>WinUsb_WritePipe</b> immediately returns, and the event is signaled when the operation is complete.

## -returns

<b>WinUsb_WritePipe</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
Indicates that an overlapped I/O operation is in progress but has not completed.  If the overlapped operation cannot be completed immediately, the function returns <b>FALSE</b> and the <b>GetLastError</b> function returns ERROR_IO_PENDING, indicating that the operation is executing in the background. Call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getoverlappedresult">WinUsb_GetOverlappedResult</a> to check the success or failure of the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The write operation initiated by  <a href="/windows/desktop/api/winusb/nf-winusb-winusb_writepipe">WinUsb_WritePipe</a> in the USB stack timed out before the operation could be completed.

</td>
</tr>
</table>

## -remarks

To create a write request, your the application must allocate a buffer, fill it with the data that you want to write to the device, and send the buffer to the host controller by calling  <b>WinUsb_WritePipe</b>. 

The following restrictions apply to the size of the buffer if  RAW_IO is  set:

<ul>
<li>The buffer length must be a multiple of the maximum endpoint packet size.</li>
<li>The length must be less than or equal to the value of MAXIMUM_TRANSFER_SIZE retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getpipepolicy">WinUsb_GetPipePolicy</a>.</li>
</ul>
There are no restrictions on the size of the buffer if RAW_IO is not set as the pipe's policy type. If the size of the buffer is greater than the maximum transfer length reported by MAXIMUM_TRANSFER_SIZE, WinUSB divides the request into smaller requests and submits them serially to the host controller.

A write request that contains zero-length data is forwarded down the USB stack. 

If an application passes <b>NULL</b> in the <i>Overlapped</i> parameter (synchronous operation), it must ensure that <i>LengthTransferred</i> is not <b>NULL</b>, even when an operation produces no output data.

If <i>Overlapped</i> is not <b>NULL</b> (asynchronous operation),  <i>LengthTransferred</i> can be set to <b>NULL</b>. For an overlapped operation (and if <i>LengthTransferred</i> is a non-<b>NULL</b> value), the value received in <i>LengthTransferred</i> after <b>WinUsb_WritePipe</b> returns is meaningless until the overlapped operation has completed. To retrieve the actual number of bytes returned, call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getoverlappedresult">WinUsb_GetOverlappedResult</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>