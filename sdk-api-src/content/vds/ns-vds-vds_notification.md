---
UID: NS:vds._VDS_NOTIFICATION
title: VDS_NOTIFICATION (vds.h)
author: windows-sdk-content
description: Defines the VDS notification structures specific to each notification target type (subject).
old-location: base\vds_notification.htm
tech.root: VDS
ms.assetid: 59d21cd3-1cff-47be-be98-f4c55f044306
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_NOTIFICATION, VDS_NOTIFICATION structure [VDS], VDS_NTT_CONTROLLER, VDS_NTT_DISK, VDS_NTT_DRIVE, VDS_NTT_DRIVE_LETTER, VDS_NTT_FILE_SYSTEM, VDS_NTT_LUN, VDS_NTT_MOUNT_POINT, VDS_NTT_PACK, VDS_NTT_PARTITION, VDS_NTT_PORT, VDS_NTT_PORTAL, VDS_NTT_PORTAL_GROUP, VDS_NTT_SUB_SYSTEM, VDS_NTT_TARGET, VDS_NTT_VOLUME, base.vds_notification, vds/_VDS_NOTIFICATION, vdshwprv/_VDS_NOTIFICATION
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_NOTIFICATION
req.redist: 
ms.custom: 19H1
---

# VDS_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the VDS 
   notification structures specific to each notification target type (subject).


## -struct-fields




### -field objectType

 Discriminant for the union enumerated by 
      <a href="https://msdn.microsoft.com/ce1f67b4-f7ea-4797-9073-0d80879c4a63">VDS_NOTIFICATION_TARGET_TYPE</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_PACK"></a><a id="vds_ntt_pack"></a><dl>
<dt><b><b>VDS_NTT_PACK</b></b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a disk pack. Use the <b>Pack</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_DISK"></a><a id="vds_ntt_disk"></a><dl>
<dt><b><b>VDS_NTT_DISK</b></b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a disk. Use the <b>Disk</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_VOLUME"></a><a id="vds_ntt_volume"></a><dl>
<dt><b><b>VDS_NTT_VOLUME</b></b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a volume. Use the <b>Volume</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_PARTITION"></a><a id="vds_ntt_partition"></a><dl>
<dt><b><b>VDS_NTT_PARTITION</b></b></dt>
<dt>60</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a partition. Use the <b>Partition</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_DRIVE_LETTER"></a><a id="vds_ntt_drive_letter"></a><dl>
<dt><b><b>VDS_NTT_DRIVE_LETTER</b></b></dt>
<dt>61</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a drive letter. Use the <b>Letter</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_FILE_SYSTEM"></a><a id="vds_ntt_file_system"></a><dl>
<dt><b><b>VDS_NTT_FILE_SYSTEM</b></b></dt>
<dt>62</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a file system. Use the <b>FileSystem</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_MOUNT_POINT"></a><a id="vds_ntt_mount_point"></a><dl>
<dt><b><b>VDS_NTT_MOUNT_POINT</b></b></dt>
<dt>63</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a drive letter  or volume GUID path. Use the <b>MountPoint</b> member 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_SUB_SYSTEM"></a><a id="vds_ntt_sub_system"></a><dl>
<dt><b><b>VDS_NTT_SUB_SYSTEM</b></b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
Used by hardware providers. The subject of the notification is a subsystem. Use the 
        <b>SubSystem</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_CONTROLLER"></a><a id="vds_ntt_controller"></a><dl>
<dt><b><b>VDS_NTT_CONTROLLER</b></b></dt>
<dt>31</dt>
</dl>
</td>
<td width="60%">
Used by hardware providers. The subject of the notification is a controller. Use the 
        <b>Controller</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_DRIVE"></a><a id="vds_ntt_drive"></a><dl>
<dt><b><b>VDS_NTT_DRIVE</b></b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
Used by hardware providers. The subject of the notification is a drive. Use the 
        <b>Drive</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_LUN"></a><a id="vds_ntt_lun"></a><dl>
<dt><b><b>VDS_NTT_LUN</b></b></dt>
<dt>33</dt>
</dl>
</td>
<td width="60%">
Used by hardware providers. The subject of the notification is a LUN. Use the 
        <b>Lun</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_PORT"></a><a id="vds_ntt_port"></a><dl>
<dt><b><b>VDS_NTT_PORT</b></b></dt>
<dt>35</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is a controller port. Use the 
        <b>Port</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_PORTAL"></a><a id="vds_ntt_portal"></a><dl>
<dt><b><b>VDS_NTT_PORTAL</b></b></dt>
<dt>36</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is an iSCSI portal. Use the 
        <b>Portal</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_TARGET"></a><a id="vds_ntt_target"></a><dl>
<dt><b><b>VDS_NTT_TARGET</b></b></dt>
<dt>37</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is an iSCSI target. Use the 
        <b>Target</b> member structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NTT_PORTAL_GROUP"></a><a id="vds_ntt_portal_group"></a><dl>
<dt><b><b>VDS_NTT_PORTAL_GROUP</b></b></dt>
<dt>38</dt>
</dl>
</td>
<td width="60%">
The subject of the notification is an iSCSI portal group. Use the 
        <b>PortalGroup</b> member structure.

</td>
</tr>
</table>
 


### -field Pack

Valid if <b>objectType</b> is <b>VDS_NTT_PACK</b>. See the 
       <a href="https://msdn.microsoft.com/3bfdef22-e3ad-4b23-9aaa-c2d08044dd25">VDS_PACK_NOTIFICATION</a> 
       structure.


### -field Disk

Valid if <b>objectType</b> is <b>VDS_NTT_DISK</b>. See the 
       <a href="https://msdn.microsoft.com/ff0069ce-611f-4ad4-9b67-adb7dc0f7abc">VDS_DISK_NOTIFICATION</a> 
       structure.


### -field Volume

Valid if <b>objectType</b> is <b>VDS_NTT_VOLUME</b>. See the 
       <a href="https://msdn.microsoft.com/0aea3de4-60b1-4452-a5f1-f3556e719e09">VDS_VOLUME_NOTIFICATION</a> 
       structure.


### -field Partition

Valid if <b>objectType</b> is <b>VDS_NTT_PARTITION</b>. See the 
       <a href="https://msdn.microsoft.com/f731d45d-e406-4a03-a604-c6ac001c341f">VDS_PARTITION_NOTIFICATION</a> 
       structure.


### -field Letter

Valid if <b>objectType</b> is <b>VDS_NTT_DRIVE_LETTER</b>. See the 
       <a href="https://msdn.microsoft.com/d64d1ba6-88a2-4418-b32c-36a84e973a06">VDS_DRIVE_LETTER_NOTIFICATION</a> 
       structure.


### -field FileSystem

Valid if <b>objectType</b> is <b>VDS_NTT_FILE_SYSTEM</b>. See the 
        <a href="https://msdn.microsoft.com/81d62c22-4f29-43f6-a00e-12502174a768">VDS_FILE_SYSTEM_NOTIFICATION</a> 
        structure.


### -field MountPoint

Valid if <b>objectType</b> is <b>VDS_NTT_MOUNT_POINT</b>. See the 
       <a href="https://msdn.microsoft.com/6e49437e-8fc7-4fc5-a227-b326a1ea9967">VDS_MOUNT_POINT_NOTIFICATION</a> 
       structure.


### -field SubSystem

Valid if <b>objectType</b> is <b>VDS_NTT_SUB_SYSTEM</b>. See the 
       <a href="https://msdn.microsoft.com/368e5b3d-11ba-400e-8dd0-929d45199dd9">VDS_SUB_SYSTEM_NOTIFICATION</a> 
       structure.


### -field Controller

Valid if <b>objectType</b> is <b>VDS_NTT_CONTROLLER</b>. See the 
       <a href="https://msdn.microsoft.com/de2aa5d8-b9b0-4e3d-9846-e886ac1d4241">VDS_CONTROLLER_NOTIFICATION</a> 
       structure.


### -field Drive

Valid if <b>objectType</b> is <b>VDS_NTT_DRIVE</b>. See the 
       <a href="https://msdn.microsoft.com/933376b3-d5eb-407b-941c-4e2b61774c1a">VDS_DRIVE_NOTIFICATION</a> 
       structure.


### -field Lun

Valid if <b>objectType</b> is <b>VDS_NTT_LUN</b>. See the 
       <a href="https://msdn.microsoft.com/42b71b32-337e-4352-b4b3-6af2caad86e5">VDS_LUN_NOTIFICATION</a> 
       structure.


### -field Port

Valid if <b>objectType</b> is <b>VDS_NTT_PORT</b>. See the 
       <a href="https://msdn.microsoft.com/4de0969f-fed5-42c7-a5f8-0bd6c58dc237">VDS_PORT_NOTIFICATION</a> 
       structure.
       

<div class="alert"><b>Note</b>  This is not supported on VDS 1.0</div>
<div> </div>

### -field Portal

Valid if <b>objectType</b> is <b>VDS_NTT_PORTAL</b>. See the 
       <a href="https://msdn.microsoft.com/53126339-a9b7-4b80-80af-ac1782dff8a8">VDS_PORTAL_NOTIFICATION</a> 
       structure.
       

<div class="alert"><b>Note</b>  This is not supported on VDS 1.0</div>
<div> </div>

### -field Target

Valid if <b>objectType</b> is <b>VDS_NTT_TARGET</b>. See the 
       <a href="https://msdn.microsoft.com/71453c9c-d6a7-4527-8988-c0388d7a9991">VDS_TARGET_NOTIFICATION</a> 
       structure.
       

<div class="alert"><b>Note</b>  This is not supported on VDS 1.0</div>
<div> </div>

### -field PortalGroup

Valid if <b>objectType</b> is <b>VDS_NTT_PORTAL_GROUP</b>. See the 
       <a href="https://msdn.microsoft.com/db4f947b-996f-4aa0-aed6-0190f00ca58a">VDS_PORTAL_GROUP_NOTIFICATION</a> 
       structure.
       

<div class="alert"><b>Note</b>  This is not supported on VDS 1.0</div>
<div> </div>

### -field Service

 




## -remarks



Applications pass this structure in the <i>pNotificationArray</i> parameter of  the 
    <a href="https://msdn.microsoft.com/0cf7bf55-922e-4092-bb2f-6423d9addb0c">IVdsAdviseSink::OnNotify</a> method.

The members of this structure are aligned on an 8-byte boundary.




## -see-also




<a href="https://msdn.microsoft.com/0cf7bf55-922e-4092-bb2f-6423d9addb0c">IVdsAdviseSink::OnNotify</a>



<a href="https://msdn.microsoft.com/ce1f67b4-f7ea-4797-9073-0d80879c4a63">VDS_NOTIFICATION_TARGET_TYPE</a>
 

 

