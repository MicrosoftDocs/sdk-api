---
UID: NF:ntmsapi.EnumerateNtmsObject
title: EnumerateNtmsObject function (ntmsapi.h)
description: The EnumerateNtmsObject function enumerates the RSM objects contained in the lpContainerId parameter.
helpviewer_keywords: ["EnumerateNtmsObject","EnumerateNtmsObject function [Files]","NTMS_CHANGER","NTMS_CHANGER_TYPE","NTMS_COMPUTER","NTMS_DRIVE","NTMS_DRIVE_TYPE","NTMS_ENUM_DEFAULT","NTMS_ENUM_ROOTPOOL","NTMS_IEDOOR","NTMS_IEPORT","NTMS_LIBRARY","NTMS_LIBREQUEST","NTMS_LOGICAL_MEDIA","NTMS_MEDIA_POOL","NTMS_MEDIA_TYPE","NTMS_OPREQUEST","NTMS_PARTITION","NTMS_PHYSICAL_MEDIA","NTMS_STORAGESLOT","_zaw_enumeratentmsobject","base.enumeratentmsobject","fs.enumeratentmsobject","ntmsapi/EnumerateNtmsObject"]
old-location: fs\enumeratentmsobject.htm
tech.root: fs
ms.assetid: bbbb2888-36f5-4667-90f0-088382ad32f5
ms.date: 12/05/2018
ms.keywords: EnumerateNtmsObject, EnumerateNtmsObject function [Files], NTMS_CHANGER, NTMS_CHANGER_TYPE, NTMS_COMPUTER, NTMS_DRIVE, NTMS_DRIVE_TYPE, NTMS_ENUM_DEFAULT, NTMS_ENUM_ROOTPOOL, NTMS_IEDOOR, NTMS_IEPORT, NTMS_LIBRARY, NTMS_LIBREQUEST, NTMS_LOGICAL_MEDIA, NTMS_MEDIA_POOL, NTMS_MEDIA_TYPE, NTMS_OPREQUEST, NTMS_PARTITION, NTMS_PHYSICAL_MEDIA, NTMS_STORAGESLOT, _zaw_enumeratentmsobject, base.enumeratentmsobject, fs.enumeratentmsobject, ntmsapi/EnumerateNtmsObject
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumerateNtmsObject
 - ntmsapi/EnumerateNtmsObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - EnumerateNtmsObject
---

# EnumerateNtmsObject function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EnumerateNtmsObject</b> function enumerates the RSM objects contained in the <i>lpContainerId</i> parameter.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpContainerId [in]

Unique identifier of the RSM object container whose objects are to be enumerated. This parameter can be the GUID of a library, media pool, partition ID, physical media, or logical media. To enumerate all objects of the type specified by the <i>dwType</i> parameter, regardless of the container, set this parameter to <b>NULL</b>. For more information about the object-container relationship, see 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

### -param lpList [out]

Buffer for the array of libraries, drives, media or other RSM object IDs.

### -param lpdwListSize [in, out]

Pointer to a variable that specifies the maximum number of IDs the function can return through the <i>lpList</i> parameter. At return time, the number of IDs in <i>lpList</i> is returned in <i>lpdwListSize</i>.

### -param dwType [in]

Type of objects to be enumerated in the <i>lpContainerId</i> container. If <i>lpContainerId</i> is <b>NULL</b>, all objects of this type supported by RSM are enumerated. This parameter can be one of the following values from the 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a> enumeration type. 



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
Changers. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_CHANGER_TYPE"></a><a id="ntms_changer_type"></a><dl>
<dt><b>NTMS_CHANGER_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Changer types. 




The <i>lpContainerId</i> parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_COMPUTER"></a><a id="ntms_computer"></a><dl>
<dt><b>NTMS_COMPUTER</b></dt>
</dl>
</td>
<td width="60%">
Current computer object. 




The <i>lpContainerId</i> parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE"></a><a id="ntms_drive"></a><dl>
<dt><b>NTMS_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
Drives. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE_TYPE"></a><a id="ntms_drive_type"></a><dl>
<dt><b>NTMS_DRIVE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Drive types. 




The <i>lpContainerId</i> parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEDOOR"></a><a id="ntms_iedoor"></a><dl>
<dt><b>NTMS_IEDOOR</b></dt>
</dl>
</td>
<td width="60%">
Doors. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEPORT"></a><a id="ntms_ieport"></a><dl>
<dt><b>NTMS_IEPORT</b></dt>
</dl>
</td>
<td width="60%">
Insert/eject ports contained in a library specified by the <i>lpContainerId</i> parameter or all the insert/eject ports supported by RSM if a <b>NULL</b> container ID is supplied. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Library objects. These include the physical library units and the offline library. 




The <i>lpContainerId</i> parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQUEST"></a><a id="ntms_librequest"></a><dl>
<dt><b>NTMS_LIBREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Library active requests (or work items) queued to the library specified by the <i>lpContainerId</i> parameter or all the library work items queued within RSM if a <b>NULL</b> container ID is supplied. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LOGICAL_MEDIA"></a><a id="ntms_logical_media"></a><dl>
<dt><b>NTMS_LOGICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
Logical media object. This is a medium allocated to an application that might contain more than one side or piece of physical media. 




The <i>lpContainerId</i> parameter must be NUL, a media pool GUID, or a partition GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_POOL"></a><a id="ntms_media_pool"></a><dl>
<dt><b>NTMS_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
Media pool object that contains logical and/or physical media, and configuration parameters to manage them. If <b>NULL</b> is specified as a container ID, only the top-level names are returned. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a media pool GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_TYPE"></a><a id="ntms_media_type"></a><dl>
<dt><b>NTMS_MEDIA_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Media type object that contains the attributes of a type of medium that is supported by RSM. Enumerating with a <b>NULL</b> will give all possible media types, not just those available on the current server. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQUEST"></a><a id="ntms_oprequest"></a><dl>
<dt><b>NTMS_OPREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Operator requests that are on this RSM server. 




The <i>lpContainerId</i> parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTITION"></a><a id="ntms_partition"></a><dl>
<dt><b>NTMS_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
Side on a piece of physical media. The piece of physical media can contain multiple physical sides (for example, an optical disk contains two sides). 




The <i>lpContainerId</i> parameter must be <b>NULL</b>, a logical media GUID, a physical media GUID, or a media pool GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PHYSICAL_MEDIA"></a><a id="ntms_physical_media"></a><dl>
<dt><b>NTMS_PHYSICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
Item of physical media (a tape, optical disk, CD-ROM, or magnetic cartridge). A piece of physical media can contain multiple physical sides (for example, sides of an optical disk). 




The <i>lpContainerId</i> parameter must be <b>NULL</b>, a media pool GUID, or a library GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_STORAGESLOT"></a><a id="ntms_storageslot"></a><dl>
<dt><b>NTMS_STORAGESLOT</b></dt>
</dl>
</td>
<td width="60%">
Media slots contained in a library specified by the <i>lpContainerId</i> parameter or all the storage slots supported by RSM if a <b>NULL</b> container ID is supplied. 




The <i>lpContainerId</i> parameter must be <b>NULL</b> or a library GUID.

</td>
</tr>
</table>

### -param dwOptions [in]

Enumeration options.   This is applicable only when <i>dwType</i> is NTMS_MEDIA_POOL.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_ENUM_ROOTPOOL"></a><a id="ntms_enum_rootpool"></a><dl>
<dt><b>NTMS_ENUM_ROOTPOOL</b></dt>
</dl>
</td>
<td width="60%">
This enumerates the root pool in addition to all other top-level media pools; it is always returned as the first GUID in the list. Enumerating the root pool is only required to get or set the security attributes on the object. <i>dwType</i> must be NTMS_MEDIA_POOL and <i>lpContainerId</i> must be <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_ENUM_DEFAULT"></a><a id="ntms_enum_default"></a><dl>
<dt><b>NTMS_ENUM_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Does not include enumeration of the root pool when enumerating the media pools.

</td>
</tr>
</table>
 

<b>Windows XP:  </b>This parameter is reserved and must be set to zero.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpdwListSize</i> pointer is missing, or <i>lpContainerId</i> is not a valid container for the object type specified by <i>dwType</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified by <i>lpdwListSize</i> is too small for all the objects found. The function truncates the list and returns the actual size in <i>lpdwListSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The GUID specified by <i>lpContainerId</i> is not the GUID of any container object in the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful. If <i>lpContainerId</i> contains no objects of the type specified by <i>dwType</i>, the function returns ERROR_SUCCESS and a <i>lpdwListSize</i> of zero.

</td>
</tr>
</table>

## -remarks

Security functions are also available to get and set specific access rights on RSM objects.

If the available number of IDs specified in the <i>lpdwListSize</i> parameter is greater than the current buffer size, <i>lpdwListSize</i> returns the number of IDs required. The application should then allocate a larger buffer and try again.

Since it is possible for IDs to be added by another process, it is possible for a subsequent function with a resized list to get an error indicating that the list is too small.

If the <i>lpContainerId</i> parameter is set to <b>NULL</b>, RSM enumerates top-level objects (such as libraries).

If more than one object is listed, the object may be enumerated from more than one container. The <b>NULL</b> container is the highest-level container and enumerates all objects in a system. For example, you can enumerate media in a particular library or all media in the system.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-createntmsmediapool">CreateNtmsMediaPool</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectsecurity">GetNtmsObjectSecurity</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectinformation">SetNtmsObjectInformation</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectsecurity">SetNtmsObjectSecurity</a>