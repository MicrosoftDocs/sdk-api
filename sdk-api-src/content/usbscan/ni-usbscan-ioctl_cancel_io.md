---
UID: NI:usbscan.IOCTL_CANCEL_IO
title: IOCTL_CANCEL_IO
author: windows-driver-content
description: Cancels activity on the specified USB transfer pipe that is associated with the specified device handle.
old-location: image\ioctl_cancel_io.htm
old-project: image
ms.assetid: 5748e949-3edb-405a-ab2f-05c929cf5aa6
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_CANCEL_IO, IOCTL_CANCEL_IO control code [Imaging Devices], image.ioctl_cancel_io, stifnc_df576f5d-a45a-4aa8-91c6-e288f9d99c14.xml, usbscan/IOCTL_CANCEL_IO
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
-	IOCTL_CANCEL_IO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IOCTL_CANCEL_IO IOCTL


## -description


Cancels activity on the specified USB transfer pipe that is associated with the specified device handle.
   
  


## -ioctlparameters




### -input-buffer

Pointer to a location containing a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff546159">PIPE_TYPE</a>.


### -input-buffer-length

Size of the input buffer.


### -output-buffer

<b>NULL</b>.


### -output-buffer-length

Zero.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



<h3><a id="ddk_ioctl_cancel_io_si"></a><a id="DDK_IOCTL_CANCEL_IO_SI"></a>DeviceIoControl Parameters
</h3>



<dl>
<dt><a id="hDevice"></a><a id="hdevice"></a><a id="HDEVICE"></a><i>hDevice</i></dt>
<dd>
Device handle, obtained by calling <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

</dd>
<dt><a id="dwIoControlCode"></a><a id="dwiocontrolcode"></a><a id="DWIOCONTROLCODE"></a><i>dwIoControlCode</i></dt>
<dd>
IOCTL_CANCEL_IO

</dd>
<dt><a id="lpInBuffer"></a><a id="lpinbuffer"></a><a id="LPINBUFFER"></a><i>lpInBuffer</i></dt>
<dd>
Pointer to a location containing a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff546159">PIPE_TYPE</a>.

</dd>
<dt><a id="nInBufferSize"></a><a id="ninbuffersize"></a><a id="NINBUFFERSIZE"></a><i>nInBufferSize</i></dt>
<dd>
Size of the input buffer.

</dd>
<dt><a id="lpOutBuffer"></a><a id="lpoutbuffer"></a><a id="LPOUTBUFFER"></a><i>lpOutBuffer</i></dt>
<dd>
<b>NULL</b>

</dd>
<dt><a id="nOutBufferSize"></a><a id="noutbuffersize"></a><a id="NOUTBUFFERSIZE"></a><i>nOutBufferSize</i></dt>
<dd>
Zero.

</dd>
<dt><a id="lpBytesReturned"></a><a id="lpbytesreturned"></a><a id="LPBYTESRETURNED"></a><i>lpBytesReturned</i></dt>
<dd>
Pointer to a location to receive the number of bytes returned.

</dd>
<dt><a id="lpOverlapped"></a><a id="lpoverlapped"></a><a id="LPOVERLAPPED"></a><i>lpOverlapped</i></dt>
<dd>
Optional pointer to an OVERLAPPED structure (described in the Microsoft Windows SDK documentation).

</dd>
</dl>


When the <b>DeviceloControl</b> function is called with the IOCTL_CANCEL_IO I/O control code, the caller must specify one of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546159">PIPE_TYPE</a>-typed values as the function's <i>lpInBuffer</i> parameter. This value indicates on which of the transfer pipes (interrupt, bulk IN, bulk OUT) the operation should be performed. For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.



