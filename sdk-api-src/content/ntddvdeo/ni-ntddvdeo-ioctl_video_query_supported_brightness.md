---
UID: NI:ntddvdeo.IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
author: windows-driver-content
description: Retrieves the supported backlight levels.
old-location: base\ioctl_video_query_supported_brightness.htm
old-project: Power
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS, IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS control code, base.ioctl_video_query_supported_brightness, ntddvdeo/IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
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
-	IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS IOCTL


## -description


Retrieves the supported backlight levels.

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
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
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



Each element in the <i>lpOutBuffer</i> array is one byte in length. Therefore, upon return, the <i>lpBytesReturned</i> parameter indicates the number of supported levels. Each level is a value from 0 to 100. The larger the value, the brighter the backlight. All levels are supported whether the power source is AC or  DC.

The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).  For information on obtaining the DDK, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84136">http://www.microsoft.com/whdc/devtools/ddk/default.mspx</a>.

Alternatively, you can define this control code as follows:

<pre class="syntax" xml:space="preserve"><code>#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/edf2b7ed-2676-483a-80ba-f148951e0e58">Backlight Control Interface</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

