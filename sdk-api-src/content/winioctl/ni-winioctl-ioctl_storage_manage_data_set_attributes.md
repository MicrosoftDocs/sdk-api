---
UID: NI:winioctl.IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
title: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
author: windows-driver-content
description: The IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code communicates attribute information to the volume manager and storage system device.
old-location: base\ioctl_storage_manage_data_set_attributes.htm
old-project: DevIO
ms.assetid: 48e797ec-dad2-4a9e-9ccd-aaa65ece8da4
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code, base.ioctl_storage_manage_data_set_attributes, winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES IOCTL


## -description


The <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
   control code communicates attribute information to the volume manager and storage system device.

To perform this operation, call the 
   <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                 IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, // dwIoControlCode
                 (LPVOID)       lpInBuffer,      // input buffer
                 (DWORD)        nInBufferSize,   // size of the input buffer
                 (LPVOID)       lpOutBuffer,     // output buffer
                 (DWORD)        nOutBufferSize,  // size of the input buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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



Use the 
    <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
    control code for sending storage system-specific information to the volume manager and storage system.

The input buffers passed through the <i>lpInBuffer</i> parameter start with a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     structure but may contain additional parameters before the list of data set ranges depending on the value of the 
     <b>Action</b> member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES</b> 
     structure. The output buffers returned 
     through the <i>lpOutBuffer</i> parameter start with a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/hh439656">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a> 
     structure but then can contain additional data depending on the value of the <b>Action</b> 
     member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</b> 
     structure pointed to by the <i>lpOutBuffer</i> parameter. These values are one of the values 
     for the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552520">DEVICE_DATA_MANAGEMENT_SET_ACTION</a> data 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff819207">DEVICE_DSM_NOTIFICATION_PARAMETERS</a>
</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadRead</b></td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439639">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451467">STORAGE_OFFLOAD_READ_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadWrite</b></td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439644">DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS</a>
</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451472">STORAGE_OFFLOAD_WRITE_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Allocation</b></td>
<td>None</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439633">DEVICE_DATA_SET_LB_PROVISIONING_STATE</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Repair</b></td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/jj602794">DEVICE_DATA_SET_REPAIR_PARAMETERS</a>
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

