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

# NtmsObjectsTypes enumeration


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NtmsObjectsTypes</b> enumeration type specifies the types of RSM objects.


## -enum-fields




### -field NTMS_UNKNOWN

Unknown  object.


### -field NTMS_OBJECT

Used internally when initializing an object.


### -field NTMS_CHANGER

Changer.


### -field NTMS_CHANGER_TYPE

Changer type.


### -field NTMS_COMPUTER

Computer.


### -field NTMS_DRIVE

Drive.


### -field NTMS_DRIVE_TYPE

Drive type.


### -field NTMS_IEDOOR

Insert/eject door.


### -field NTMS_IEPORT

Insert/eject port.


### -field NTMS_LIBRARY

Library (including the offline library).


### -field NTMS_LIBREQUEST

Library request.


### -field NTMS_LOGICAL_MEDIA

Logical media.


### -field NTMS_MEDIA_POOL

Media pool.


### -field NTMS_MEDIA_TYPE

Media type.


### -field NTMS_PARTITION

Side of a piece of physical media.


### -field NTMS_PHYSICAL_MEDIA

Physical media.


### -field NTMS_STORAGESLOT

Storage slot.


### -field NTMS_OPREQUEST

Operator request.


### -field NTMS_UI_DESTINATION

User interface destination.


### -field NTMS_NUMBER_OF_OBJECT_TYPES




## -remarks



The following table show the relationship of RSM objects.

<table>
<tr>
<th>Container</th>
<th>Object</th>
</tr>
<tr>
<td>Library</td>
<td>Changer</td>
</tr>
<tr>
<td></td>
<td>Door</td>
</tr>
<tr>
<td></td>
<td>Drive</td>
</tr>
<tr>
<td></td>
<td>Library request</td>
</tr>
<tr>
<td></td>
<td>Media type</td>
</tr>
<tr>
<td></td>
<td>Physical media</td>
</tr>
<tr>
<td></td>
<td>Port</td>
</tr>
<tr>
<td></td>
<td>Slot</td>
</tr>
<tr>
<td>Logical media</td>
<td>Side</td>
</tr>
<tr>
<td>Media pool</td>
<td>Logical media</td>
</tr>
<tr>
<td></td>
<td>Media pool</td>
</tr>
<tr>
<td></td>
<td>Physical media</td>
</tr>
<tr>
<td>NULL</td>
<td>Changer</td>
</tr>
<tr>
<td></td>
<td>Changer type</td>
</tr>
<tr>
<td></td>
<td>Computer</td>
</tr>
<tr>
<td></td>
<td>Door</td>
</tr>
<tr>
<td></td>
<td>Drive</td>
</tr>
<tr>
<td></td>
<td>Drive type</td>
</tr>
<tr>
<td></td>
<td>Library</td>
</tr>
<tr>
<td></td>
<td>Library request</td>
</tr>
<tr>
<td></td>
<td>Logical media</td>
</tr>
<tr>
<td></td>
<td>Media pool (free, unrecognized, import, and application root)</td>
</tr>
<tr>
<td></td>
<td>Media type</td>
</tr>
<tr>
<td></td>
<td>Operator request</td>
</tr>
<tr>
<td></td>
<td>Port</td>
</tr>
<tr>
<td></td>
<td>Physical media</td>
</tr>
<tr>
<td></td>
<td>Side</td>
</tr>
<tr>
<td>Physical Media</td>
<td>Side</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a>



<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a>
 

 

