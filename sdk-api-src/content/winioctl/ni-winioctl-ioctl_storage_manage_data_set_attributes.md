---
UID: NI:winioctl.IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
title: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
description: The IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code communicates attribute information to the volume manager and storage system device.helpviewer_keywords: ["IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES","IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control","IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code","base.ioctl_storage_manage_data_set_attributes","winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES"]
old-location: base\ioctl_storage_manage_data_set_attributes.htm
tech.root: devio
ms.assetid: 48e797ec-dad2-4a9e-9ccd-aaa65ece8da4
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code, base.ioctl_storage_manage_data_set_attributes, winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
f1_keywords:
- winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES IOCTL


## -description


The <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
   control code communicates attribute information to the volume manager and storage system device.

To perform this operation, call the 
   <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



Use the 
    <b>IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</b> 
    control code for sending storage system-specific information to the volume manager and storage system.

The input buffers passed through the <i>lpInBuffer</i> parameter start with a 
     <a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     structure but may contain additional parameters before the list of data set ranges depending on the value of the 
     <b>Action</b> member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES</b> 
     structure. The output buffers returned 
     through the <i>lpOutBuffer</i> parameter start with a 
     <a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a> 
     structure but then can contain additional data depending on the value of the <b>Action</b> 
     member of the 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</b> 
     structure pointed to by the <i>lpOutBuffer</i> parameter. These values are one of the values 
     for the 
     <a href="https://docs.microsoft.com/windows/desktop/DevIO/device-data-management-set-action">DEVICE_DATA_MANAGEMENT_SET_ACTION</a> data 
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
<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_dsm_notification_parameters">DEVICE_DSM_NOTIFICATION_PARAMETERS</a>
</td>
<td>None</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadRead</b></td>
<td>
<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_dsm_offload_read_parameters">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_offload_read_output">STORAGE_OFFLOAD_READ_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_OffloadWrite</b></td>
<td>
<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_dsm_offload_write_parameters">DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_offload_write_output">STORAGE_OFFLOAD_WRITE_OUTPUT</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Allocation</b></td>
<td>None</td>
<td>
<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_data_set_lb_provisioning_state">DEVICE_DATA_SET_LB_PROVISIONING_STATE</a>
</td>
</tr>
<tr>
<td><b>DeviceDsmAction_Repair</b></td>
<td>
<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_data_set_repair_parameters">DEVICE_DATA_SET_REPAIR_PARAMETERS</a>
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




<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

