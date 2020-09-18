---
UID: NI:winioctl.IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
title: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
description: The IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code communicates attribute information to the volume manager and storage system device.
helpviewer_keywords: ["IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES","IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control","IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code","base.ioctl_storage_manage_data_set_attributes","winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES"]
old-location: base\ioctl_storage_manage_data_set_attributes.htm
tech.root: base
ms.assetid: 48e797ec-dad2-4a9e-9ccd-aaa65ece8da4
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control, IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code, base.ioctl_storage_manage_data_set_attributes, winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
 - winioctl/IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES
---

# IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES IOCTL


## -description

The **IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES** control code communicates attribute information to the volume manager and storage system device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to device
  IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES, // dwIoControlCode
  (LPVOID) lpInBuffer,                      // input buffer
  (DWORD) nInBufferSize,                    // size of the input buffer
  (LPVOID) lpOutBuffer,                     // output buffer
  (DWORD) nOutBufferSize,                   // size of the input buffer
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped               // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

Use the **IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES** control code for sending storage system-specific information to the volume manager and storage system.

The input buffers passed through the *lpInBuffer* parameter start with a [DEVICE_MANAGE_DATA_SET_ATTRIBUTES](ns-winioctl-device_manage_data_set_attributes.md) structure but may contain additional parameters before the list of data set ranges depending on the value of the **Action** member of the **DEVICE_MANAGE_DATA_SET_ATTRIBUTES** structure. The output buffers returned through the *lpOutBuffer* parameter start with a [DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT](ns-winioctl-device_manage_data_set_attributes.md) structure but then can contain additional data depending on the value of the **Action** member of the **DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT** structure pointed to by the *lpOutBuffer* parameter. These values are one of the values for the [DEVICE_DATA_MANAGEMENT_SET_ACTION](/windows/desktop/DevIO/device-data-management-set-action) data type.

Value | Parameters structure | Output block structure
------|----------------------|-----------------------
**DeviceDsmAction_Trim** | None | None
**DeviceDsmAction_Notification** | [DEVICE_DSM_NOTIFICATION_PARAMETERS](ns-winioctl-device_dsm_notification_parameters.md) | None
**DeviceDsmAction_OffloadRead** | [DEVICE_DSM_OFFLOAD_READ_PARAMETERS](ns-winioctl-device_dsm_offload_read_parameters.md) | [STORAGE_OFFLOAD_READ_OUTPUT](ns-winioctl-storage_offload_read_output.md)
**DeviceDsmAction_OffloadWrite** | [DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS](ns-winioctl-device_dsm_offload_write_parameters.md) | [STORAGE_OFFLOAD_WRITE_OUTPUT](ns-winioctl-storage_offload_write_output.md)
**DeviceDsmAction_Allocation** | None | [DEVICE_DATA_SET_LB_PROVISIONING_STATE](ns-winioctl-device_data_set_lb_provisioning_state.md)
**DeviceDsmAction_Repair** | [DEVICE_DATA_SET_REPAIR_PARAMETERS](ns-winioctl-device_data_set_repair_parameters.md) | None
**DeviceDsmAction_Scrub** | None | None
**DeviceDsmAction_Resiliency** | None | None

## -see-also

* [DEVICE_MANAGE_DATA_SET_ATTRIBUTES](ns-winioctl-device_manage_data_set_attributes.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)