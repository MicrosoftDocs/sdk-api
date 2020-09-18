---
UID: NS:winioctl._DEVICE_DSM_NOTIFICATION_PARAMETERS
title: DEVICE_DSM_NOTIFICATION_PARAMETERS
description: Contains parameters for the DeviceDsmAction_Notification action for the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PDEVICE_DSM_NOTIFICATION_PARAMETERS","DEVICE_DSM_NOTIFICATION_PARAMETERS","DEVICE_DSM_NOTIFICATION_PARAMETERS structure","DEVICE_DSM_NOTIFY_FLAG_BEGIN","DEVICE_DSM_NOTIFY_FLAG_END","FILE_TYPE_NOTIFICATION_GUID_CRASHDUMP_FILE","FILE_TYPE_NOTIFICATION_GUID_HIBERNATION_FILE","FILE_TYPE_NOTIFICATION_GUID_PAGE_FILE","PDEVICE_DSM_NOTIFICATION_PARAMETERS","PDEVICE_DSM_NOTIFICATION_PARAMETERS structure pointer","base.device_dsm_notification_parameters","winioctl/DEVICE_DSM_NOTIFICATION_PARAMETERS","winioctl/PDEVICE_DSM_NOTIFICATION_PARAMETERS"]
old-location: base\device_dsm_notification_parameters.htm
tech.root: base
ms.assetid: 42f76bab-0260-4b43-a8cf-02faedb7e672
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DSM_NOTIFICATION_PARAMETERS, DEVICE_DSM_NOTIFICATION_PARAMETERS, DEVICE_DSM_NOTIFICATION_PARAMETERS structure, DEVICE_DSM_NOTIFY_FLAG_BEGIN, DEVICE_DSM_NOTIFY_FLAG_END, FILE_TYPE_NOTIFICATION_GUID_CRASHDUMP_FILE, FILE_TYPE_NOTIFICATION_GUID_HIBERNATION_FILE, FILE_TYPE_NOTIFICATION_GUID_PAGE_FILE, PDEVICE_DSM_NOTIFICATION_PARAMETERS, PDEVICE_DSM_NOTIFICATION_PARAMETERS structure pointer, base.device_dsm_notification_parameters, winioctl/DEVICE_DSM_NOTIFICATION_PARAMETERS, winioctl/PDEVICE_DSM_NOTIFICATION_PARAMETERS'
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
req.typenames: DEVICE_DSM_NOTIFICATION_PARAMETERS, *PDEVICE_DSM_NOTIFICATION_PARAMETERS
req.redist: 
f1_keywords:
 - _DEVICE_DSM_NOTIFICATION_PARAMETERS
 - winioctl/_DEVICE_DSM_NOTIFICATION_PARAMETERS
 - PDEVICE_DSM_NOTIFICATION_PARAMETERS
 - winioctl/PDEVICE_DSM_NOTIFICATION_PARAMETERS
 - DEVICE_DSM_NOTIFICATION_PARAMETERS
 - winioctl/DEVICE_DSM_NOTIFICATION_PARAMETERS
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
 - DEVICE_DSM_NOTIFICATION_PARAMETERS
---

# DEVICE_DSM_NOTIFICATION_PARAMETERS structure


## -description

Contains parameters for the <b>DeviceDsmAction_Notification</b> action for the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.

## -struct-fields

### -field Size

Specifies the total size, in bytes, of this structure. The value of this member must include the total 
      size, in bytes, of the <b>FileTypeIDs</b> member.

### -field Flags

Flags specific to the notify operation

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_DSM_NOTIFY_FLAG_BEGIN"></a><a id="device_dsm_notify_flag_begin"></a><dl>
<dt><b>DEVICE_DSM_NOTIFY_FLAG_BEGIN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The ranges specified in the 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-device_data_set_range">DEVICE_DATA_SET_RANGE</a> structures following the 
        <a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
        structure are currently being used by the file types that are specified in the 
        <b>FileTypeIDs</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_DSM_NOTIFY_FLAG_END"></a><a id="device_dsm_notify_flag_end"></a><dl>
<dt><b>DEVICE_DSM_NOTIFY_FLAG_END</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The ranges are no longer being used by the file types that are specified in the 
        <b>FileTypeIDs</b> member.

</td>
</tr>
</table>

### -field NumFileTypeIDs

The number of entries in the <b>FileTypeIDs</b> member.

### -field FileTypeID

One or more <b>GUID</b> values that specify the file type for the notification 
       operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_TYPE_NOTIFICATION_GUID_PAGE_FILE"></a><a id="file_type_notification_guid_page_file"></a><dl>
<dt><b>FILE_TYPE_NOTIFICATION_GUID_PAGE_FILE</b></dt>
<dt>0d0a64a1-38fc-4db8-9fe7-3f4352cd7c5c</dt>
</dl>
</td>
<td width="60%">
Specifies a notification operation for a page file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_TYPE_NOTIFICATION_GUID_HIBERNATION_FILE"></a><a id="file_type_notification_guid_hibernation_file"></a><dl>
<dt><b>FILE_TYPE_NOTIFICATION_GUID_HIBERNATION_FILE</b></dt>
<dt>b7624d64-b9a3-4cf8-8011-5b86c940e7b7</dt>
</dl>
</td>
<td width="60%">
Specifies a notification operation for the system hibernation file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_TYPE_NOTIFICATION_GUID_CRASHDUMP_FILE"></a><a id="file_type_notification_guid_crashdump_file"></a><dl>
<dt><b>FILE_TYPE_NOTIFICATION_GUID_CRASHDUMP_FILE</b></dt>
<dt>9d453eb7-d2a6-4dbd-a2e3-fbd0ed9109a9</dt>
</dl>
</td>
<td width="60%">
Specifies a notification operation for a system crash dump file.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>