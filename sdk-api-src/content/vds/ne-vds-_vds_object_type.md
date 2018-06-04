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

# _VDS_OBJECT_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of 
   valid types of a VDS object.


## -enum-fields




### -field VDS_OT_UNKNOWN

This value is reserved.


### -field VDS_OT_PROVIDER

The object is a <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a>.


### -field VDS_OT_PACK

The object is a <a href="https://msdn.microsoft.com/e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9">disk pack</a>.


### -field VDS_OT_VOLUME

The object is a <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume</a>.


### -field VDS_OT_VOLUME_PLEX

The object is a <a href="https://msdn.microsoft.com/9e770bfc-2bcb-45f0-a7fc-ba526349839e">volume plex</a>.


### -field VDS_OT_DISK

The object is a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915271">disk</a>.


### -field VDS_OT_SUB_SYSTEM

The object is a <a href="https://msdn.microsoft.com/f605a5de-9256-4b43-8e12-3d78fd6cd9f1">subsystem</a>.


### -field VDS_OT_CONTROLLER

The object is a <a href="https://msdn.microsoft.com/ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8">controller</a>.


### -field VDS_OT_DRIVE

The object is a <a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">drive</a>.


### -field VDS_OT_LUN

The object is a <a href="https://msdn.microsoft.com/ea22bd6d-4a7a-4674-82e9-08460914ff8e">LUN</a>.


### -field VDS_OT_LUN_PLEX

The object is a <a href="https://msdn.microsoft.com/db6eabaa-1b84-4613-ab2a-8d5904305e08">LUN plex</a>.


### -field VDS_OT_PORT

The object is a <a href="https://msdn.microsoft.com/5f94bcdc-93ab-4522-88bd-009a049b5dc9">controller port</a>.


### -field VDS_OT_PORTAL

The object is an <a href="https://msdn.microsoft.com/6655bbae-07d3-416b-9e45-ddcbe3433f40">iSCSI portal</a>.


### -field VDS_OT_TARGET

The object is an <a href="https://msdn.microsoft.com/e88d65ad-9b56-4620-a0f5-573c5e245b3e">iSCSI target</a>.


### -field VDS_OT_PORTAL_GROUP

The object is an <a href="https://msdn.microsoft.com/e5892e96-b6ad-447a-9627-b44fc6f1b27a">iSCSI portal group</a>.


### -field VDS_OT_STORAGE_POOL

The object is a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_OT_HBAPORT

The object is an <a href="startup_and_service_objects.htm">HBA port</a>.


### -field VDS_OT_INIT_ADAPTER

The object is an <a href="startup_and_service_objects.htm">iSCSI initiator adapter</a>.


### -field VDS_OT_INIT_PORTAL

The object is an <a href="startup_and_service_objects.htm">iSCSI initiator portal</a>.


### -field VDS_OT_ASYNC

This value is reserved.


### -field VDS_OT_ENUM

This value is reserved.


### -field VDS_OT_VDISK

The object is a virtual disk.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_OT_OPEN_VDISK

This value is reserved.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


## -remarks



The <a href="https://msdn.microsoft.com/3f346255-c5c6-4ca3-9718-0347c3f8294a">IVdsProviderPrivate::GetObject</a> 
    and <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> methods pass a <b>VDS_OBJECT_TYPE</b> 
    value as an argument to indicate an object type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_OBJECT_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_OBJECT_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3f346255-c5c6-4ca3-9718-0347c3f8294a">IVdsProviderPrivate::GetObject</a>



<a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

