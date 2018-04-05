---
UID: NI:ntddvdeo.IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
author: windows-driver-content
description: Retrieves the current AC and DC backlight levels and the current power state.
old-location: base\ioctl_video_query_display_brightness.htm
old-project: Power
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS, IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS control code, base.ioctl_video_query_display_brightness, ntddvdeo/IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddvdeo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_READ_CAPACITY, PSTORAGE_READ_CAPACITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntddvdeo.h
api_name:
-	IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS IOCTL


## -description


<p class="CCE_Message">[This control code is available for use in the operating systems specified in the Requirements section. Support for this control code was removed in Windows Server 2008 and Windows Vista. Use the <a href="https://msdn.microsoft.com/01fa3efc-2a1d-4405-989f-2c180842c6b9">WmiMonitorBrightness</a> class instead.]

Retrieves the current AC and DC backlight levels and the current power state.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);</pre>
</td>
</tr>
</table></span></div>

## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).  For information on obtaining the DDK, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84136">http://www.microsoft.com/whdc/devtools/ddk/default.mspx</a>.

Alternatively, you can define this control code as follows:

<pre class="syntax" xml:space="preserve"><code>#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/edf2b7ed-2676-483a-80ba-f148951e0e58">Backlight Control Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554041">DISPLAY_BRIGHTNESS</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568140">IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS</a>
 

 

