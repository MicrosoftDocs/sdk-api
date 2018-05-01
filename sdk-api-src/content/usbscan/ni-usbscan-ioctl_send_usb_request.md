---
UID: NI:usbscan.IOCTL_SEND_USB_REQUEST
title: IOCTL_SEND_USB_REQUEST
author: windows-driver-content
description: Sends a vendor-defined request to a USB device, using the control pipe, and optionally sends or receives additional data.
old-location: image\ioctl_send_usb_request.htm
old-project: image
ms.assetid: 27e22a21-cd89-43e8-8ce1-448c0f4c4d78
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_SEND_USB_REQUEST, IOCTL_SEND_USB_REQUEST control code [Imaging Devices], image.ioctl_send_usb_request, stifnc_2532cbfa-8373-4666-8a87-fac7923513bd.xml, usbscan/IOCTL_SEND_USB_REQUEST
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: usbscan.h
req.include-header: Usbscan.h
req.target-type: Windows
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
req.typenames: RAW_PIPE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usbscan.h
api_name:
-	IOCTL_SEND_USB_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IOCTL_SEND_USB_REQUEST IOCTL


## -description



Sends a vendor-defined request to a USB device, using the control pipe, and optionally sends or receives additional data.




## -ioctlparameters




### -input-buffer

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542928">IO_BLOCK_EX</a> structure.


### -input-buffer-length

Size of the input buffer.


### -output-buffer

Pointer to the same buffer the <b>pbyData</b> member of the IO_BLOCK_EX structure identified, or <b>NULL</b> if a data transfer is not being requested.


### -output-buffer-length

Size of the output buffer, or zero if a data transfer is not being requested.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



<h3><a id="ddk_ioctl_send_usb_request_si"></a><a id="DDK_IOCTL_SEND_USB_REQUEST_SI"></a>DeviceIoControl Parameters</h3>


When the <b>DeviceloControl</b> function is called with the IOCTL_SEND_USB_REQUEST control code, the caller must specify the address of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542928">IO_BLOCK_EX</a> structure as the function's <i>lpInBuffer</i> parameter. The type of request specified with this I/O control code is device-specific and vendor-defined, as are the type and size of any information that might be sent or received.

The following table shows how input arguments should be specified.

<table>
<tr>
<th>Argument</th>
<th>Read Operation</th>
<th>Write Operation</th>
<th>No Data Transfer</th>
</tr>
<tr>
<td>
<i>lpInBuffer</i>

</td>
<td>
IO_BLOCK_EX pointer.

</td>
<td>
IO_BLOCK_EX pointer.

</td>
<td>
IO_BLOCK_EX pointer.

</td>
</tr>
<tr>
<td>
<i>lpOutBuffer</i>

</td>
<td>
Pointer to buffer that will receive data to be read.

</td>
<td>
Pointer to buffer containing data to be written.

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
<i>lpOutBufferSize</i>

</td>
<td>
Size of buffer.

</td>
<td>
Size of buffer.

</td>
<td>
Zero

</td>
</tr>
<tr>
<td>
<b>bRequest</b> member of IO_BLOCK_EX structure

</td>
<td>
Device-specific request code.

</td>
<td>
Device-specific request code.

</td>
<td>
Device-specific request code.

</td>
</tr>
<tr>
<td>
<b>pbyData</b> member of IO_BLOCK_EX structure

</td>
<td>
Same pointer as <i>lpOutBuffer</i>.

</td>
<td>
Same pointer as <i>lpOutBuffer</i>.

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
<b>uLength</b> member of IO_BLOCK_EX structure

</td>
<td>
Same value as <i>lpOutBufferSize</i>.

</td>
<td>
Same value as <i>lpOutBufferSize</i>.

</td>
<td>
Zero

</td>
</tr>
<tr>
<td>
<b>fTransferDirectionIn</b> member of IO_BLOCK_EX structure

</td>
<td>
<b>TRUE</b>

</td>
<td>
<b>FALSE</b>

</td>
<td>
<b>FALSE</b>

</td>
</tr>
</table>
 

Note that the <b>bmRequestType</b> member of the IO_BLOCK_EX structure is not used with IOCTL_SEND_USB_REQUEST.

Using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542928">IO_BLOCK_EX</a> structure contents, the kernel-mode driver creates a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538923">URB</a> that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540393">_URB_CONTROL_VENDOR_OR_CLASS_REQUEST</a> structure.

The following table indicates the values assigned to _URB_CONTROL_VENDOR_OR_CLASS_REQUEST structure members.

<table>
<tr>
<th>Structure Member</th>
<th>Value Assigned</th>
</tr>
<tr>
<td>
<b>TransferFlags</b>

</td>
<td>
0

</td>
</tr>
<tr>
<td>
<b>TransferBufferLength</b>

</td>
<td>
<i>pIoBlockEx</i>-&gt;<b>uLength</b>

</td>
</tr>
<tr>
<td>
<b>TransferBuffer</b>

</td>
<td>
<i>lpOutBuffer</i> (read) or

<i>pIoBlockEx</i>-&gt;<b>pbyData</b> (write)

</td>
</tr>
<tr>
<td>
<b>TransferBufferMDL</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
<b>RequestTypeReservedBits</b>

</td>
<td>
0xC0 (read) or

0x40 (write)

</td>
</tr>
<tr>
<td>
<b>Request</b>

</td>
<td>
<i>pIoBlockEx</i>-&gt;<b>bRequest</b>

</td>
</tr>
<tr>
<td>
<b>Value</b>

</td>
<td>
(<b>SHORT</b>)<i>pIoBlockEx</i>-&gt;<b>uOffset</b>

</td>
</tr>
<tr>
<td>
<b>Index</b>

</td>
<td>
<i>pIoBlockEx</i>-&gt;<b>uIndex</b>

</td>
</tr>
</table>
 

For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.



