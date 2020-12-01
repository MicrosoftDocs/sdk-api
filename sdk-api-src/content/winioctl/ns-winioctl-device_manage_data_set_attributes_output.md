---
UID: NS:winioctl._DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
title: DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
description: Output structure for the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PDEVICE_DSM_OUTPUT","*PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT","DEVICE_DSM_OUTPUT","DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT","DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT structure","DeviceDsmAction_Allocation","DeviceDsmAction_Notification","DeviceDsmAction_OffloadRead","DeviceDsmAction_OffloadWrite","DeviceDsmAction_Repair","DeviceDsmAction_Resiliency","DeviceDsmAction_Scrub","DeviceDsmAction_Trim","PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT","PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT structure pointer","base.device_manage_data_set_attributes_output","winioctl/DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT","winioctl/PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT"]
old-location: base\device_manage_data_set_attributes_output.htm
tech.root: base
ms.assetid: a3f03509-8be9-4cb4-b942-f5ab358bd70e
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DSM_OUTPUT, *PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, DEVICE_DSM_OUTPUT, DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT structure, DeviceDsmAction_Allocation, DeviceDsmAction_Notification, DeviceDsmAction_OffloadRead, DeviceDsmAction_OffloadWrite, DeviceDsmAction_Repair, DeviceDsmAction_Resiliency, DeviceDsmAction_Scrub, DeviceDsmAction_Trim, PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT structure pointer, base.device_manage_data_set_attributes_output, winioctl/DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, winioctl/PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, *PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT, DEVICE_DSM_OUTPUT, *PDEVICE_DSM_OUTPUT
req.redist: 
f1_keywords:
 - _DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
 - winioctl/_DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
 - PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
 - winioctl/PDEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
 - DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
 - winioctl/DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
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
 - DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT
---

# DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT structure


## -description

Output structure for the 
     <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     control code.

## -struct-fields

### -field Size

Size of the structure. This is set to 
      <code>sizeof(DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT)</code>.

### -field Action

The action related to the instance of this structure. This is a value for the 
      <a href="/windows/desktop/DevIO/device-data-management-set-action">DEVICE_DATA_MANAGEMENT_SET_ACTION</a> data
      type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Trim"></a><a id="devicedsmaction_trim"></a><a id="DEVICEDSMACTION_TRIM"></a><dl>
<dt><b>DeviceDsmAction_Trim</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A trim action is performed. This value is not supported for user-mode applications.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Notification"></a><a id="devicedsmaction_notification"></a><a id="DEVICEDSMACTION_NOTIFICATION"></a><dl>
<dt><b>DeviceDsmAction_Notification</b></dt>
<dt>2 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000002)</dt>
</dl>
</td>
<td width="60%">
A notification action is performed. The <b>DeviceDsmActionFlag_NonDestructive</b> 
        (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_OffloadRead"></a><a id="devicedsmaction_offloadread"></a><a id="DEVICEDSMACTION_OFFLOADREAD"></a><dl>
<dt><b>DeviceDsmAction_OffloadRead</b></dt>
<dt>3 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000003)</dt>
</dl>
</td>
<td width="60%">
An offload read action is performed. The output described by the 
         <b>OutputBlockOffset</b> and <b>OutputBlockLength</b> members is a 
         <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_read_output">STORAGE_OFFLOAD_READ_OUTPUT</a> structure. 
         The <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000000) is a bit flag to indicate to 
         the driver stack that this operation is non-destructive.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_OffloadWrite"></a><a id="devicedsmaction_offloadwrite"></a><a id="DEVICEDSMACTION_OFFLOADWRITE"></a><dl>
<dt><b>DeviceDsmAction_OffloadWrite</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
An offload write action is performed. The output described by the 
         <b>OutputBlockOffset</b> and <b>OutputBlockLength</b> members is a 
         <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_write_output">STORAGE_OFFLOAD_WRITE_OUTPUT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Allocation"></a><a id="devicedsmaction_allocation"></a><a id="DEVICEDSMACTION_ALLOCATION"></a><dl>
<dt><b>DeviceDsmAction_Allocation</b></dt>
<dt>5 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000005)</dt>
</dl>
</td>
<td width="60%">
An allocation bitmap is returned for the first data set range passed in. The output is in a 
         <a href="/windows/win32/api/winioctl/ns-winioctl-device_data_set_lb_provisioning_state">DEVICE_DATA_SET_LB_PROVISIONING_STATE</a> 
         structure. The <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000000) is a bit flag to 
         indicate to the driver stack that this operation is non-destructive.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Repair"></a><a id="devicedsmaction_repair"></a><a id="DEVICEDSMACTION_REPAIR"></a><dl>
<dt><b>DeviceDsmAction_Repair</b></dt>
<dt>6 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000006)</dt>
</dl>
</td>
<td width="60%">
A repair action is performed. The <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000000) 
         is a bit flag to indicate to the driver stack that this operation is non-destructive.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Scrub"></a><a id="devicedsmaction_scrub"></a><a id="DEVICEDSMACTION_SCRUB"></a><dl>
<dt><b>DeviceDsmAction_Scrub</b></dt>
<dt>7 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000007)</dt>
</dl>
</td>
<td width="60%">
A scrub action is performed. The <b>DeviceDsmActionFlag_NonDestructive</b> 
         (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="DeviceDsmAction_Resiliency"></a><a id="devicedsmaction_resiliency"></a><a id="DEVICEDSMACTION_RESILIENCY"></a><dl>
<dt><b>DeviceDsmAction_Resiliency</b></dt>
<dt>8 | <b>DeviceDsmActionFlag_NonDestructive</b> (0x80000008)</dt>
</dl>
</td>
<td width="60%">
A resiliency action is performed. The <b>DeviceDsmActionFlag_NonDestructive</b> 
         (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
</table>

### -field Flags

Not used.

### -field OperationStatus

Not used.

### -field ExtendedError

Extended error information.

### -field TargetDetailedError

Target specific error.

### -field ReservedStatus

Reserved.

### -field OutputBlockOffset

The offset, in bytes, from the beginning of this structure to where any action-specific data is 
      located.

### -field OutputBlockLength

The length, in bytes, of the action-specific data.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-device_data_set_range">DEVICE_DATA_SET_RANGE</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>