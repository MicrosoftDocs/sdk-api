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

# _VDS_NOTIFICATION_TARGET_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of the valid target types (subjects) of a VDS notification.


## -enum-fields




### -field VDS_NTT_UNKNOWN

This value is reserved.


### -field VDS_NTT_PACK

The target is a disk pack. This value corresponds to the <b>VDS_OT_PACK</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_VOLUME

The target is a volume. This value corresponds to the <b>VDS_OT_VOLUME</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_DISK

The target is a disk. This value corresponds to the <b>VDS_OT_DISK</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_PARTITION

The target is a partition.


### -field VDS_NTT_DRIVE_LETTER

The target is a drive letter.


### -field VDS_NTT_FILE_SYSTEM

The target is a file system.


### -field VDS_NTT_MOUNT_POINT

The target is a drive letter  or volume GUID path.


### -field VDS_NTT_SUB_SYSTEM

The target is a subsystem. This value corresponds to the <b>VDS_OT_SUB_SYSTEM</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_CONTROLLER

The target is a controller. This value corresponds to the <b>VDS_OT_CONTROLLER</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_DRIVE

The target is a drive. This value corresponds to the <b>VDS_OT_DRIVE</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_LUN

The target is a LUN. This value corresponds to the <b>VDS_OT_LUN</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.


### -field VDS_NTT_PORT

The target is a controller port.
       This value corresponds to the <b>VDS_OT_PORT</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.

<div class="alert"><b>Note</b>  This value is not supported on VDS 1.0.</div>
<div> </div>

### -field VDS_NTT_PORTAL

The target is an iSCSI portal.
       This value corresponds to the <b>VDS_OT_PORTAL</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.

<div class="alert"><b>Note</b>  This value is not supported on VDS 1.0.</div>
<div> </div>

### -field VDS_NTT_TARGET

The target is a target.
       This value corresponds to the <b>VDS_OT_TARGET</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.

<div class="alert"><b>Note</b>  This value is not supported on VDS 1.0.</div>
<div> </div>

### -field VDS_NTT_PORTAL_GROUP

The target is an iSCSI portal group.
       This value corresponds to the <b>VDS_PORTAL_GROUP</b> value in the  <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.

<div class="alert"><b>Note</b>  This value is not supported on VDS 1.0.</div>
<div> </div>

### -field VDS_NTT_SERVICE

This member is not currently used.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes a <b>VDS_NOTIFICATION_TARGET_TYPE</b> 
    value as a member to indicate a notification type. Some values in the <b>VDS_NOTIFICATION_TARGET_TYPE</b> correspond to values in the <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration. For the integer value of a VDS object type, 
    such as a volume or LUN object, see the 
    <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a> enumeration.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_NOTIFICATION_TARGET_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_NOTIFICATION_TARGET_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a>
 

 

