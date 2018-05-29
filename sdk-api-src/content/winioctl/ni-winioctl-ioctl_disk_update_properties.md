---
UID: NI:winioctl.IOCTL_DISK_UPDATE_PROPERTIES
title: IOCTL_DISK_UPDATE_PROPERTIES
author: windows-sdk-content
description: Invalidates the cached partition table and re-enumerates the device.
old-location: fs\ioctl_disk_update_properties.htm
old-project: FileIO
ms.assetid: d97e0257-c3b0-48d5-b801-594763be8178
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IOCTL_DISK_UPDATE_PROPERTIES, IOCTL_DISK_UPDATE_PROPERTIES control, IOCTL_DISK_UPDATE_PROPERTIES control code [Files], _win32_ioctl_disk_update_properties, base.ioctl_disk_update_properties, fs.ioctl_disk_update_properties, winioctl/IOCTL_DISK_UPDATE_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	IOCTL_DISK_UPDATE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_UPDATE_PROPERTIES IOCTL


## -description


Invalidates the cached partition table and re-enumerates the device.

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
  IOCTL_DISK_UPDATE_PROPERTIES,// dwIoControlCode
  NULL,                        // lpInBuffer
  0,                           // nInBufferSize
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize
  (LPDWORD)lpBytesReturned,    // lpBytesReturned
  (LPDWORD) lpOverlapped       // lpOverlapped
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



This operation is used in synchronizing the system view of the specified disk device when the partition table of the disk is directly modified. 
			Be sure to perform this operation when you update the usable space for a disk so that the system will update its partition table.

You can update the properties of  a live volume, and the volume can be open for sharing during the update operation.

You do not need to lock a volume that you are updating, nor do you need to shut down other applications or services during the update operation.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>
 

 

