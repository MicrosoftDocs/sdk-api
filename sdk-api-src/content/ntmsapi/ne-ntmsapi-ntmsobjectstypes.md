---
UID: NE:ntmsapi.NtmsObjectsTypes
title: NtmsObjectsTypes (ntmsapi.h)
description: The NtmsObjectsTypes enumeration type specifies the types of RSM objects.
helpviewer_keywords: ["NTMS_CHANGER","NTMS_CHANGER_TYPE","NTMS_COMPUTER","NTMS_DRIVE","NTMS_DRIVE_TYPE","NTMS_IEDOOR","NTMS_IEPORT","NTMS_LIBRARY","NTMS_LIBREQUEST","NTMS_LOGICAL_MEDIA","NTMS_MEDIA_POOL","NTMS_MEDIA_TYPE","NTMS_OBJECT","NTMS_OPREQUEST","NTMS_PARTITION","NTMS_PHYSICAL_MEDIA","NTMS_STORAGESLOT","NTMS_UI_DESTINATION","NTMS_UNKNOWN","NtmsObjectsTypes","NtmsObjectsTypes enumeration [Files]","_zaw_ntmsobjectstypes","base.ntmsobjectstypes","fs.ntmsobjectstypes","ntmsapi/NTMS_CHANGER","ntmsapi/NTMS_CHANGER_TYPE","ntmsapi/NTMS_COMPUTER","ntmsapi/NTMS_DRIVE","ntmsapi/NTMS_DRIVE_TYPE","ntmsapi/NTMS_IEDOOR","ntmsapi/NTMS_IEPORT","ntmsapi/NTMS_LIBRARY","ntmsapi/NTMS_LIBREQUEST","ntmsapi/NTMS_LOGICAL_MEDIA","ntmsapi/NTMS_MEDIA_POOL","ntmsapi/NTMS_MEDIA_TYPE","ntmsapi/NTMS_OBJECT","ntmsapi/NTMS_OPREQUEST","ntmsapi/NTMS_PARTITION","ntmsapi/NTMS_PHYSICAL_MEDIA","ntmsapi/NTMS_STORAGESLOT","ntmsapi/NTMS_UI_DESTINATION","ntmsapi/NTMS_UNKNOWN","ntmsapi/NtmsObjectsTypes"]
old-location: fs\ntmsobjectstypes.htm
tech.root: fs
ms.assetid: 598e7cb1-f463-4252-9bdf-ccb98f36f4da
ms.date: 12/05/2018
ms.keywords: NTMS_CHANGER, NTMS_CHANGER_TYPE, NTMS_COMPUTER, NTMS_DRIVE, NTMS_DRIVE_TYPE, NTMS_IEDOOR, NTMS_IEPORT, NTMS_LIBRARY, NTMS_LIBREQUEST, NTMS_LOGICAL_MEDIA, NTMS_MEDIA_POOL, NTMS_MEDIA_TYPE, NTMS_OBJECT, NTMS_OPREQUEST, NTMS_PARTITION, NTMS_PHYSICAL_MEDIA, NTMS_STORAGESLOT, NTMS_UI_DESTINATION, NTMS_UNKNOWN, NtmsObjectsTypes, NtmsObjectsTypes enumeration [Files], _zaw_ntmsobjectstypes, base.ntmsobjectstypes, fs.ntmsobjectstypes, ntmsapi/NTMS_CHANGER, ntmsapi/NTMS_CHANGER_TYPE, ntmsapi/NTMS_COMPUTER, ntmsapi/NTMS_DRIVE, ntmsapi/NTMS_DRIVE_TYPE, ntmsapi/NTMS_IEDOOR, ntmsapi/NTMS_IEPORT, ntmsapi/NTMS_LIBRARY, ntmsapi/NTMS_LIBREQUEST, ntmsapi/NTMS_LOGICAL_MEDIA, ntmsapi/NTMS_MEDIA_POOL, ntmsapi/NTMS_MEDIA_TYPE, ntmsapi/NTMS_OBJECT, ntmsapi/NTMS_OPREQUEST, ntmsapi/NTMS_PARTITION, ntmsapi/NTMS_PHYSICAL_MEDIA, ntmsapi/NTMS_STORAGESLOT, ntmsapi/NTMS_UI_DESTINATION, ntmsapi/NTMS_UNKNOWN, ntmsapi/NtmsObjectsTypes
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtmsObjectsTypes
 - ntmsapi/NtmsObjectsTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NtmsObjectsTypes
---

# NtmsObjectsTypes enumeration


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NtmsObjectsTypes</b> enumeration type specifies the types of RSM objects.

## -enum-fields

### -field NTMS_UNKNOWN:0

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

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a>
