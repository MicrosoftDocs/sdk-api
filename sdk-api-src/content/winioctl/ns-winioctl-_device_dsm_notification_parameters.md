---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DEVICE_DSM_NOTIFICATION_PARAMETERS structure


## -description


Contains parameters for the <b>DeviceDsmAction_Notification</b> action for the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff552523">DEVICE_DATA_SET_RANGE</a> structures following the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>
 

 

