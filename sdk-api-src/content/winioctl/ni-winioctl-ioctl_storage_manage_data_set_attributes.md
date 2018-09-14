---
UID: NI:winioctl.IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
title: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
author: windows-sdk-content
description: The IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code communicates attribute information to the volume manager and storage system device.
old-location: base\ioctl_storage_manage_data_set_attributes.htm
tech.root: devio
ms.assetid: 48e797ec-dad2-4a9e-9ccd-aaa65ece8da4
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code, base.ioctl_storage_manage_data_set_attributes, winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES IOCTL


## -description


The <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
   control code communicates attribute information to the volume manager and storage system device.

To perform this operation, call the 
   <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.

```cpp
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                 IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, // dwIoControlCode
                 (LPVOID)       lpInBuffer,      // input buffer
                 (DWORD)        nInBufferSize,   // size of the input buffer
                 (LPVOID)       lpOutBuffer,     // output buffer
                 (DWORD)        nOutBufferSize,  // size of the input buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



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



Use the 
    <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
    control code for sending storage system-specific information to the volume manager and storage system.

The input buffers passed through the <i>lpInBuffer</i> parameter start with a 
     <a href="https://msdn.microsoft.com/328902b7-97e3-40dc-9771-f5e64ccf3364">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     structure but may contain additional parameters before the list of data set ranges depending on the value of the 
     <b>Action</b> member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES</b> 
     structure. The output buffers returned 
     through the <i>lpOutBuffer</i> parameter start with a 
     <a href="https://msdn.microsoft.com/a3f03509-8be9-4cb4-b942-f5ab358bd70e">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a> 
     structure but then can contain additional data depending on the value of the <b>Action</b> 
     member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</b> 
     structure pointed to by the <i>lpOutBuffer</i> parameter. These values are one of the values 
     for the 
     <a href="https://msdn.microsoft.com/ff688c9a-8669-4699-aab9-1e2e3a5c7fca">DEVICE_DATA_MANAGEMENT_SET_ACTION</a> data 
     type.

<table>
<tr>
<th>Value</th>
<th>Parameters structure</th>
<th>Output block structure</th>
</tr>
<tr>
<td><b>DeviceDsmAction_Trim</b></td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Notification</b></td>
<td>
<a href="https://msdn.microsoft.com/42f76bab-0260-4b43-a8cf-02faedb7e672">DEVICE_DSM_NOTIFICATION_PARAMETERS</a>
</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadRead</b></td>
<td>
<a href="https://msdn.microsoft.com/20dd3e5b-90f4-45fc-8cc8-bf9e6d08a026">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/93eaa8dd-b244-4fdd-abd4-c7cab46cb2a6">STORAGE_OFFLOAD_READ_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadWrite</b></td>
<td>
<a href="https://msdn.microsoft.com/d0107cae-50c9-46d2-97cd-324030692903">DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/9da3ac28-93fd-45b7-9ebe-1436593bf591">STORAGE_OFFLOAD_WRITE_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Allocation</b></td>
<td>None</td>
<td>
<a href="https://msdn.microsoft.com/757ffd97-2a00-4508-817c-0bfb2f2e3a84">DEVICE_DATA_SET_LB_PROVISIONING_STATE</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Repair</b></td>
<td>
<a href="https://msdn.microsoft.com/95bc892c-9bb7-464c-8084-7cc6e643fa28">DEVICE_DATA_SET_REPAIR_PARAMETERS</a>
</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Scrub</b></td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Resiliency</b></td>
<td>None</td>
<td>None</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/328902b7-97e3-40dc-9771-f5e64ccf3364">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

