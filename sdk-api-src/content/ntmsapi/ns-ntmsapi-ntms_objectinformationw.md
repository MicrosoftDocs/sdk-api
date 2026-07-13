---
UID: NS:ntmsapi._NTMS_OBJECTINFORMATIONW
title: NTMS_OBJECTINFORMATIONW (ntmsapi.h)
description: The NTMS_OBJECTINFORMATION structure defines the properties that an application can get and set for RSM devices, media and system controls (such as libraries, drives, media, operator requests). This is the common structure of objects in the RSM database. (Unicode)
helpviewer_keywords: ["*LPNTMS_OBJECTINFORMATIONW","LPNTMS_OBJECTINFORMATION","LPNTMS_OBJECTINFORMATION structure pointer [Files]","NTMS_CHANGER","NTMS_CHANGER_TYPE","NTMS_COMPUTER","NTMS_DRIVE","NTMS_DRIVE_TYPE","NTMS_IEDOOR","NTMS_IEPORT","NTMS_LIBRARY","NTMS_LIBREQUEST","NTMS_LOGICAL_MEDIA","NTMS_MEDIA_POOL","NTMS_MEDIA_TYPE","NTMS_NEEDS_SERVICE","NTMS_NOT_PRESENT","NTMS_OBJECTINFORMATION","NTMS_OBJECTINFORMATION structure [Files]","NTMS_OBJECTINFORMATIONA","NTMS_OBJECTINFORMATIONW","NTMS_OPREQUEST","NTMS_PARTITION","NTMS_PHYSICAL_MEDIA","NTMS_READY","NTMS_STORAGESLOT","_NTMS_OBJECTINFORMATIONA","_NTMS_OBJECTINFORMATIONW","_zaw_ntms_objectinformation","base.ntms_objectinformation","fs.ntms_objectinformation","ntmsapi/LPNTMS_OBJECTINFORMATION","ntmsapi/NTMS_OBJECTINFORMATION"]
old-location: fs\ntms_objectinformation.htm
tech.root: fs
ms.assetid: 56e3380b-47c7-4861-bb2b-31d67ac10fe1
ms.date: 12/05/2018
ms.keywords: '*LPNTMS_OBJECTINFORMATIONW, LPNTMS_OBJECTINFORMATION, LPNTMS_OBJECTINFORMATION structure pointer [Files], NTMS_CHANGER, NTMS_CHANGER_TYPE, NTMS_COMPUTER, NTMS_DRIVE, NTMS_DRIVE_TYPE, NTMS_IEDOOR, NTMS_IEPORT, NTMS_LIBRARY, NTMS_LIBREQUEST, NTMS_LOGICAL_MEDIA, NTMS_MEDIA_POOL, NTMS_MEDIA_TYPE, NTMS_NEEDS_SERVICE, NTMS_NOT_PRESENT, NTMS_OBJECTINFORMATION, NTMS_OBJECTINFORMATION structure [Files], NTMS_OBJECTINFORMATIONA, NTMS_OBJECTINFORMATIONW, NTMS_OPREQUEST, NTMS_PARTITION, NTMS_PHYSICAL_MEDIA, NTMS_READY, NTMS_STORAGESLOT, _NTMS_OBJECTINFORMATIONA, _NTMS_OBJECTINFORMATIONW, _zaw_ntms_objectinformation, base.ntms_objectinformation, fs.ntms_objectinformation, ntmsapi/LPNTMS_OBJECTINFORMATION, ntmsapi/NTMS_OBJECTINFORMATION'
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
req.typenames: NTMS_OBJECTINFORMATIONW, *LPNTMS_OBJECTINFORMATIONW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_OBJECTINFORMATIONW
 - ntmsapi/_NTMS_OBJECTINFORMATIONW
 - LPNTMS_OBJECTINFORMATIONW
 - ntmsapi/LPNTMS_OBJECTINFORMATIONW
 - NTMS_OBJECTINFORMATIONW
 - ntmsapi/NTMS_OBJECTINFORMATIONW
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
 - NTMS_OBJECTINFORMATION
 - NTMS_OBJECTINFORMATIONA
 - NTMS_OBJECTINFORMATIONW
---

# NTMS_OBJECTINFORMATIONW structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_OBJECTINFORMATION</b> structure defines the properties that an application can get and set for RSM devices, media and system controls (such as libraries, drives, media, operator requests). This is the common structure of objects in the RSM database.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

Size of the information structure, in bytes. This member must be set to the correct size of the structure prior to using either the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a> function or the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a> function.

### -field dwType

Type: <b>DWORD</b>

Type of device or system control for which to get/set information. This member must be set to one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_CHANGER"></a><a id="ntms_changer"></a><dl>
<dt><b>NTMS_CHANGER</b></dt>
</dl>
</td>
<td width="60%">
A changer object represents the robotic element of a library unit. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_changerinformationa">NTMS_CHANGERINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_CHANGER_TYPE"></a><a id="ntms_changer_type"></a><dl>
<dt><b>NTMS_CHANGER_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A changer type object is created for each unique changer device type attached to a system. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_changertypeinformationa">NTMS_CHANGERTYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_COMPUTER"></a><a id="ntms_computer"></a><dl>
<dt><b>NTMS_COMPUTER</b></dt>
</dl>
</td>
<td width="60%">
The current computer object. There is no structure for the computer object. The <b>Info</b> member is a pointer to an <a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_computerinformation">NTMS_COMPUTERINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE"></a><a id="ntms_drive"></a><dl>
<dt><b>NTMS_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
A drive object represents a tape drive or disk drive. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_driveinformationa">NTMS_DRIVEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE_TYPE"></a><a id="ntms_drive_type"></a><dl>
<dt><b>NTMS_DRIVE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A drive type object is created for each unique drive device type attached to a system. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_drivetypeinformationa">NTMS_DRIVETYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEDOOR"></a><a id="ntms_iedoor"></a><dl>
<dt><b>NTMS_IEDOOR</b></dt>
</dl>
</td>
<td width="60%">
An NTMS_IEDOOR object represents the door-access mechanism of a library unit. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_iedoorinformation">NTMS_IEDOORINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEPORT"></a><a id="ntms_ieport"></a><dl>
<dt><b>NTMS_IEPORT</b></dt>
</dl>
</td>
<td width="60%">
An NTMS_IEPORT object represents the insert/eject port of a library unit. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_ieportinformation">NTMS_IEPORTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
A library object represents an online or offline library. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_libraryinformation">NTMS_LIBRARYINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQUEST"></a><a id="ntms_librequest"></a><dl>
<dt><b>NTMS_LIBREQUEST</b></dt>
</dl>
</td>
<td width="60%">
A library request object is created for each request for a library to perform an action. A list of library requests is maintained by RSM as a queue of work to be performed. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_librequestinformationa">NTMS_LIBREQUESTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LOGICAL_MEDIA"></a><a id="ntms_logical_media"></a><dl>
<dt><b>NTMS_LOGICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The primary handle used by applications to access the specified medium. In the case of multi-sided media, each side is treated as an individual piece of physical media. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_lmidinformation">NTMS_LMIDINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_POOL"></a><a id="ntms_media_pool"></a><dl>
<dt><b>NTMS_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
A media pool is a logical grouping of media. All media in a media pool must be the same media type. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_mediapoolinformation">NTMS_MEDIAPOOLINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_TYPE"></a><a id="ntms_media_type"></a><dl>
<dt><b>NTMS_MEDIA_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A media type object is created for each unique media type in a system. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_mediatypeinformation">NTMS_MEDIATYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQUEST"></a><a id="ntms_oprequest"></a><dl>
<dt><b>NTMS_OPREQUEST</b></dt>
</dl>
</td>
<td width="60%">
An operator request object represents an RSM request for a user to get the information. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_oprequestinformationa">NTMS_OPREQUESTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTITION"></a><a id="ntms_partition"></a><dl>
<dt><b>NTMS_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
A side object represents a side of a piece of physical media. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_partitioninformationa">NTMS_PARTITIONINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PHYSICAL_MEDIA"></a><a id="ntms_physical_media"></a><dl>
<dt><b>NTMS_PHYSICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
A physical media object represents a magnetic tape or removable disk. A piece of physical media can contain one or more sides. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_pmidinformationa">NTMS_PMIDINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_STORAGESLOT"></a><a id="ntms_storageslot"></a><dl>
<dt><b>NTMS_STORAGESLOT</b></dt>
</dl>
</td>
<td width="60%">
A storage slot object represents one of the slots that can hold the specified medium in a library. The <b>Info</b> member is a pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_storageslotinformation">NTMS_STORAGESLOTINFORMATION</a> structure.

</td>
</tr>
</table>

### -field Created

Type: <b>SYSTEMTIME</b>

Date/time stamp when the object was created.

### -field Modified

Type: <b>SYSTEMTIME</b>

Date/time stamp when the object was modified.

### -field ObjectGuid

Type: <b>NTMS_GUID</b>

GUID of the object.

### -field Enabled

Type: <b>BOOL</b>

Indicates whether the device or system control object is enabled.

### -field dwOperationalState

Type: <b>DWORD</b>

Defines the current operational state of the object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_NOT_PRESENT"></a><a id="ntms_not_present"></a><dl>
<dt><b>NTMS_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
This device or object is not currently present.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_READY"></a><a id="ntms_ready"></a><dl>
<dt><b>NTMS_READY</b></dt>
</dl>
</td>
<td width="60%">
This device or object is available and ready.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_NEEDS_SERVICE"></a><a id="ntms_needs_service"></a><dl>
<dt><b>NTMS_NEEDS_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
This device or object has failed and needs service.

</td>
</tr>
</table>

### -field szName

Type: <b>TCHAR[NTMS_OBJECTNAME_LENGTH]</b>

Name of the media, device, or system control object. Media pool and logical media names can be changed using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a> function. All other object names are read-only.

### -field szDescription

Type: <b>TCHAR[NTMS_DESCRIPTION_LENGTH]</b>

Description of the device or system control object. The description of device and system control objects can be changed using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a> function. (Writable for all objects)

### -field Info.Drive.case

### -field Info.Drive.case.NTMS_DRIVE

### -field Info.DriveType.case

### -field Info.DriveType.case.NTMS_DRIVE_TYPE

### -field Info.Library.case

### -field Info.Library.case.NTMS_LIBRARY

### -field Info.Changer.case

### -field Info.Changer.case.NTMS_CHANGER

### -field Info.ChangerType.case

### -field Info.ChangerType.case.NTMS_CHANGER_TYPE

### -field Info.StorageSlot.case

### -field Info.StorageSlot.case.NTMS_STORAGESLOT

### -field Info.IEDoor.case

### -field Info.IEDoor.case.NTMS_IEDOOR

### -field Info.IEPort.case

### -field Info.IEPort.case.NTMS_IEPORT

### -field Info.PhysicalMedia.case

### -field Info.PhysicalMedia.case.NTMS_PHYSICAL_MEDIA

### -field Info.LogicalMedia.case

### -field Info.LogicalMedia.case.NTMS_LOGICAL_MEDIA

### -field Info.Partition.case

### -field Info.Partition.case.NTMS_PARTITION

### -field Info.MediaPool.case

### -field Info.MediaPool.case.NTMS_MEDIA_POOL

### -field Info.MediaType.case

### -field Info.MediaType.case.NTMS_MEDIA_TYPE

### -field Info.LibRequest.case

### -field Info.LibRequest.case.NTMS_LIBREQUEST

### -field Info.OpRequest.case

### -field Info.OpRequest.case.NTMS_OPREQUEST

### -field Info.Computer.case

### -field Info.Computer.case.NTMS_COMPUTER



### -field Info

Device or system control object-specific information. The format of this information depends on the <b>dwType</b> member.

### -field Info.Drive

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_driveinformationa">NTMS_DRIVEINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_DRIVE</b>.

### -field Info.DriveType

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_drivetypeinformationa">NTMS_DRIVETYPEINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_DRIVE_TYPE</b>.

### -field Info.Library

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_libraryinformation">NTMS_LIBRARYINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_LIBRARY</b>.

### -field Info.Changer

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_changerinformationa">NTMS_CHANGERINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_CHANGER</b>.

### -field Info.ChangerType

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_changertypeinformationa">NTMS_CHANGERTYPEINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_CHANGER_TYPE</b>.

### -field Info.StorageSlot

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_storageslotinformation">NTMS_STORAGESLOTINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_STORAGESLOT</b>.

### -field Info.IEDoor

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_iedoorinformation">NTMS_IEDOORINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_IEDOOR</b>.

### -field Info.IEPort

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_ieportinformation">NTMS_IEPORTINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_IEPORT</b>.

### -field Info.PhysicalMedia

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_pmidinformationa">NTMS_PMIDINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_PHYSICAL_MEDIA</b>.

### -field Info.LogicalMedia

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_lmidinformation">NTMS_LMIDINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_LOGICAL_MEDIA</b>.

### -field Info.Partition

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_partitioninformationa">NTMS_PARTITIONINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_PARTITION</b>.

### -field Info.MediaPool

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_mediapoolinformation">NTMS_MEDIAPOOLINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_MEDIA_POOL</b>.

### -field Info.MediaType

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_mediatypeinformation">NTMS_MEDIATYPEINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_MEDIA_TYPE</b>.

### -field Info.LibRequest

Type: <b><a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_librequestinformationa">NTMS_LIBREQUESTINFORMATION</a></b>

This format is used if the <b>dwType</b> value is <b>NTMS_LIBREQUEST</b>.

### -field Info.OpRequest

Type: <b>NTMS_OPREQUESTINFORMATION</b>

This format is used if the <b>dwType</b> value is <b>NTMS_OPREQUEST</b>.

### -field Info.Computer

## -remarks

All members of the 
<b>NTMS_OBJECTINFORMATION</b> structure are read-only at the RSM function-level unless specified as WRITABLE in the definition of the member.





> [!NOTE]
> The ntmsapi.h header defines NTMS_OBJECTINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a>
