---
UID: NI:ntddvdeo.IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
author: windows-driver-content
description: Sets the current AC and DC backlight levels.
old-location: base\ioctl_video_set_display_brightness.htm
old-project: Power
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS control code, base.ioctl_video_set_display_brightness, ntddvdeo/IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddvdeo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
-	IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS IOCTL


## -description


Sets the current AC and DC backlight levels.

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
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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



The values specified in the <b>ucACBrightness</b> and <b>ucDCBrightness</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554041">DISPLAY_BRIGHTNESS</a> structure must have been previously returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff567831">IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS</a>. For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.

The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).  For information on obtaining the DDK, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84136">http://www.microsoft.com/whdc/devtools/ddk/default.mspx</a>.

Alternatively, you can define this control code as follows:

<pre class="syntax" xml:space="preserve"><code>#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/edf2b7ed-2676-483a-80ba-f148951e0e58">Backlight Control Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554041">DISPLAY_BRIGHTNESS</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567822">IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567831">IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS</a>
 

 

