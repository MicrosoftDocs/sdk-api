---
UID: NS:ntmsapi._NTMS_LIBRARYINFORMATION
title: NTMS_LIBRARYINFORMATION (ntmsapi.h)
description: The NTMS_LIBRARYINFORMATION structure defines properties specific to a library object.
helpviewer_keywords: ["NTMS_INVENTORY_FAST","NTMS_INVENTORY_NONE","NTMS_INVENTORY_OMID","NTMS_LIBRARYFLAG_CLEANERPRESENT","NTMS_LIBRARYFLAG_FIXEDOFFLINE","NTMS_LIBRARYFLAG_IGNORECLEANERUSESREMAINING","NTMS_LIBRARYFLAG_RECOGNIZECLEANERBARCODE","NTMS_LIBRARYINFORMATION","NTMS_LIBRARYINFORMATION structure [Files]","NTMS_LIBRARYTYPE_OFFLINE","NTMS_LIBRARYTYPE_ONLINE","NTMS_LIBRARYTYPE_STANDALONE","NTMS_LIBRARYTYPE_UNKNOWN","_zaw_ntms_libraryinformation","base.ntms_libraryinformation","fs.ntms_libraryinformation","ntmsapi/NTMS_LIBRARYINFORMATION"]
old-location: fs\ntms_libraryinformation.htm
tech.root: fs
ms.assetid: f8ca33ba-35e2-4fd9-a9a0-1393bbbede80
ms.date: 12/05/2018
ms.keywords: NTMS_INVENTORY_FAST, NTMS_INVENTORY_NONE, NTMS_INVENTORY_OMID, NTMS_LIBRARYFLAG_CLEANERPRESENT, NTMS_LIBRARYFLAG_FIXEDOFFLINE, NTMS_LIBRARYFLAG_IGNORECLEANERUSESREMAINING, NTMS_LIBRARYFLAG_RECOGNIZECLEANERBARCODE, NTMS_LIBRARYINFORMATION, NTMS_LIBRARYINFORMATION structure [Files], NTMS_LIBRARYTYPE_OFFLINE, NTMS_LIBRARYTYPE_ONLINE, NTMS_LIBRARYTYPE_STANDALONE, NTMS_LIBRARYTYPE_UNKNOWN, _zaw_ntms_libraryinformation, base.ntms_libraryinformation, fs.ntms_libraryinformation, ntmsapi/NTMS_LIBRARYINFORMATION
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
req.typenames: NTMS_LIBRARYINFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_LIBRARYINFORMATION
 - ntmsapi/_NTMS_LIBRARYINFORMATION
 - NTMS_LIBRARYINFORMATION
 - ntmsapi/NTMS_LIBRARYINFORMATION
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
 - NTMS_LIBRARYINFORMATION
---

# NTMS_LIBRARYINFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_LIBRARYINFORMATION</b> structure defines properties specific to a library object.

## -struct-fields

### -field LibraryType

Library type object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYTYPE_ONLINE"></a><a id="ntms_librarytype_online"></a><dl>
<dt><b>NTMS_LIBRARYTYPE_ONLINE</b></dt>
</dl>
</td>
<td width="60%">
A robotic element that automates the mounting and dismounting of media into one or more drives.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYTYPE_STANDALONE"></a><a id="ntms_librarytype_standalone"></a><dl>
<dt><b>NTMS_LIBRARYTYPE_STANDALONE</b></dt>
</dl>
</td>
<td width="60%">
A stand-alone drive that is modeled as a library with one drive in RSM.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYTYPE_OFFLINE"></a><a id="ntms_librarytype_offline"></a><dl>
<dt><b>NTMS_LIBRARYTYPE_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
Media that is not in a library is in the offline library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYTYPE_UNKNOWN"></a><a id="ntms_librarytype_unknown"></a><dl>
<dt><b>NTMS_LIBRARYTYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Library type cannot be determined.

</td>
</tr>
</table>

### -field CleanerSlot

For each library, this represents the slot that was assigned to the cleaner cartridge. If this member is <b>NULL</b>, there is no cleaner slot defined for this library.

### -field CleanerSlotDefault

Represents a libraries' default or preferred cleaner slot. If <b>NULL</b>, there is not a preferred slot.

### -field LibrarySupportsDriveCleaning

Used by drives that require cleaning under robotics control. If <b>TRUE</b>, automatic drive cleaning operations are enabled.

### -field BarCodeReaderInstalled

Returns <b>TRUE</b> if a bar code reader is installed in a library; otherwise returns <b>FALSE</b>.

### -field InventoryMethod

Default or user-selected method for performing inventory of this library. (This member is writable.) This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_FAST"></a><a id="ntms_inventory_fast"></a><dl>
<dt><b>NTMS_INVENTORY_FAST</b></dt>
</dl>
</td>
<td width="60%">
If the library has a bar-code reader installed, this value causes a bar-code inventory to be performed. If the library does not have a bar-code reader, this flag causes a differential inventory to be performed (slots which transitioned from empty to full are classified).

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_OMID"></a><a id="ntms_inventory_omid"></a><dl>
<dt><b>NTMS_INVENTORY_OMID</b></dt>
</dl>
</td>
<td width="60%">
A full inventory involves mounting each side in a library and reading the on-media identification from the media. This type of inventory can be very time consuming for some library units.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_NONE"></a><a id="ntms_inventory_none"></a><dl>
<dt><b>NTMS_INVENTORY_NONE</b></dt>
</dl>
</td>
<td width="60%">
After the library door is closed, no inventory is performed. Inventory might be required if a mount label-check fails.

</td>
</tr>
</table>

### -field dwCleanerUsesRemaining

Number of uses remaining on the cleaner in the library. This member is zero if no cleaner is present or if the library does not support cleaning.

### -field FirstDriveNumber

Number of the first drive in the library.

### -field dwNumberOfDrives

Number of drives in the library.

### -field FirstSlotNumber

Number of the first slot in the library.

### -field dwNumberOfSlots

Number of slots in the library.

### -field FirstDoorNumber

Number of the first access door in the library.

### -field dwNumberOfDoors

Number of access doors in the library.

### -field FirstPortNumber

Number of the first insert/eject port in the library.

### -field dwNumberOfPorts

Number of insert/eject ports in the library.

### -field FirstChangerNumber

Number of the first changer in the library.

### -field dwNumberOfChangers

Number of changers in the library.

### -field dwNumberOfMedia

Number of media in the online or offline library.

### -field dwNumberOfMediaTypes

Number of media types supported by the library.

### -field dwNumberOfLibRequests

Number of current library requests.

### -field Reserved

Reserved.

### -field AutoRecovery

If this member is <b>TRUE</b>, a full inventory will be performed if a mount fails. The failure may be either hardware or label mismatch. For ATAPI CD libraries, this parameter cannot be disabled. The default is <b>TRUE</b>. Large library owners should disable this feature.

### -field dwFlags

This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYFLAG_FIXEDOFFLINE"></a><a id="ntms_libraryflag_fixedoffline"></a><dl>
<dt><b>NTMS_LIBRARYFLAG_FIXEDOFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library is an offline library, not a library that is not present.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYFLAG_CLEANERPRESENT"></a><a id="ntms_libraryflag_cleanerpresent"></a><dl>
<dt><b>NTMS_LIBRARYFLAG_CLEANERPRESENT</b></dt>
</dl>
</td>
<td width="60%">
A cleaner is present in the changer.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYFLAG_IGNORECLEANERUSESREMAINING"></a><a id="ntms_libraryflag_ignorecleanerusesremaining"></a><dl>
<dt><b>NTMS_LIBRARYFLAG_IGNORECLEANERUSESREMAINING</b></dt>
</dl>
</td>
<td width="60%">
The cleaner cartridge will be used until it no longer cleans the drive, instead of keeping track of the number of cleanings left.  Do not set this flag directly.  It is set or cleared based on the value of <b>dwCleanerUsesRemaining</b>.  It is set if <b>dwCleanerUsesRemaining</b> is 0xFFFFFFFF, and cleared otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARYFLAG_RECOGNIZECLEANERBARCODE"></a><a id="ntms_libraryflag_recognizecleanerbarcode"></a><dl>
<dt><b>NTMS_LIBRARYFLAG_RECOGNIZECLEANERBARCODE</b></dt>
</dl>
</td>
<td width="60%">
Treat barcoded cartridges that have CLN as a prefix as cleaner cartridges, instead of  mounting them in the drive to identify them. 

</td>
</tr>
</table>

## -remarks

For offline libraries, only <b>LibraryType</b> and <b>dwNumberOfMedia</b> are reported. All other values should be ignored.

The 
<b>NTMS_LIBRARYINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>