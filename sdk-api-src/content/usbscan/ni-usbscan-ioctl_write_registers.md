---
UID: NI:usbscan.IOCTL_WRITE_REGISTERS
title: IOCTL_WRITE_REGISTERS
author: windows-driver-content
description: Writes to USB device registers, using the control pipe.
old-location: image\ioctl_write_registers.htm
old-project: image
ms.assetid: c7175b39-9db2-4903-bb50-bb0c97fda471
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_WRITE_REGISTERS, IOCTL_WRITE_REGISTERS control code [Imaging Devices], image.ioctl_write_registers, stifnc_e994c3b6-35b9-4b5f-aaba-72fedeb9e08f.xml, usbscan/IOCTL_WRITE_REGISTERS
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
-	IOCTL_WRITE_REGISTERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IOCTL_WRITE_REGISTERS IOCTL


## -description


Writes to USB device registers, using the control pipe.


## -ioctlparameters




### -input-buffer

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542924">IO_BLOCK</a> structure.


### -input-buffer-length

Size of the input buffer.


### -output-buffer

<b>NULL</b>


### -output-buffer-length

Zero.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



<h3><a id="ddk_ioctl_write_registers_si"></a><a id="DDK_IOCTL_WRITE_REGISTERS_SI"></a>DeviceIoControl Parameters</h3>


When the <b>DeviceloControl</b> function is called with the IOCTL_WRITE_REGISTERS I/O control code, the caller must specify the address of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542924">IO_BLOCK</a> structure as the function's <i>lpInBuffer</i> parameter.

Using the IO_BLOCK contents, the kernel-mode driver creates a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538923">URB</a> that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540393">_URB_CONTROL_VENDOR_OR_CLASS_REQUEST</a> structure.

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
<i>pIoBlock</i>-&gt;<b>uLength</b>

</td>
</tr>
<tr>
<td>
<b>TransferBuffer</b>

</td>
<td>
<i>pIoBlock</i>-&gt;<b>pbyData</b>

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
0x40

</td>
</tr>
<tr>
<td>
<b>Request</b>

</td>
<td>
(<i>pIoBlock</i>-&gt;<b>uLength</b> &gt; 1) ? 0x04 : 0x0C

</td>
</tr>
<tr>
<td>
<b>Value</b>

</td>
<td>
(SHORT)<i>pIoBlock</i>-&gt;<b>uOffset</b>

</td>
</tr>
<tr>
<td>
<b>Index</b>

</td>
<td>
<i>pIoBlock</i>-&gt;<b>uIndex</b>

</td>
</tr>
</table>
 

For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD             cbRet;
BOOL              bRet;
IO_BLOCK          IoBlock;
OVERLAPPED        overlapped;

IoBlock.uOffset = (BYTE)byOffset;
IoBlock.uLength = (BYTE)byNbOfReg;
IoBlock.pbyData = pbyData;

memset(&amp;overlapped, 0, sizeof(OVERLAPPED));
overlapped.hEvent = 
    CreateEvent(NULL,    // pointer to security attributes
                         // WIN95 ignores this parameter
                FALSE,   // automatic reset
                FALSE,   // initialize to not signaled
                NULL);   // pointer to the event-object name

bRet = DeviceIoControl( DeviceHandle,
                        (DWORD) IOCTL_WRITE_REGISTERS,
                        &amp;IoBlock,
                        sizeof(IO_BLOCK),
                        NULL,
                        0,
                        &amp;cbRet,
                        &amp;overlapped);

if( bRet == TRUE )
{
    WaitForSingleObject(overlapped.hEvent, INFINITE);
    // we do not the test, the result is zero
}

CloseHandle(overlapped.hEvent);</pre>
</td>
</tr>
</table></span></div>


