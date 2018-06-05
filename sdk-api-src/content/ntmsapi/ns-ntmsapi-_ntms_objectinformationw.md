---
UID: NS:ntmsapi._NTMS_OBJECTINFORMATIONW
title: "_NTMS_OBJECTINFORMATIONW"
author: windows-sdk-content
description: The NTMS_OBJECTINFORMATION structure defines the properties that an application can get and set for RSM devices, media and system controls (such as libraries, drives, media, operator requests). This is the common structure of objects in the RSM database.
old-location: fs\ntms_objectinformation.htm
old-project: Rsm
ms.assetid: 56e3380b-47c7-4861-bb2b-31d67ac10fe1
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: "*LPNTMS_OBJECTINFORMATIONW, LPNTMS_OBJECTINFORMATION, LPNTMS_OBJECTINFORMATION structure pointer [Files], NTMS_CHANGER, NTMS_CHANGER_TYPE, NTMS_COMPUTER, NTMS_DRIVE, NTMS_DRIVE_TYPE, NTMS_IEDOOR, NTMS_IEPORT, NTMS_LIBRARY, NTMS_LIBREQUEST, NTMS_LOGICAL_MEDIA, NTMS_MEDIA_POOL, NTMS_MEDIA_TYPE, NTMS_NEEDS_SERVICE, NTMS_NOT_PRESENT, NTMS_OBJECTINFORMATION, NTMS_OBJECTINFORMATION structure [Files], NTMS_OBJECTINFORMATIONW, NTMS_OPREQUEST, NTMS_PARTITION, NTMS_PHYSICAL_MEDIA, NTMS_READY, NTMS_STORAGESLOT, _NTMS_OBJECTINFORMATIONA, _NTMS_OBJECTINFORMATIONW, _zaw_ntms_objectinformation, base.ntms_objectinformation, fs.ntms_objectinformation, ntmsapi/LPNTMS_OBJECTINFORMATION, ntmsapi/NTMS_OBJECTINFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: NTMS_OBJECTINFORMATIONW, *LPNTMS_OBJECTINFORMATIONW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntmsapi.h
api_name:
-	NTMS_OBJECTINFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NTMS_OBJECTINFORMATIONW structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_OBJECTINFORMATION</b> structure defines the properties that an application can get and set for RSM devices, media and system controls (such as libraries, drives, media, operator requests). This is the common structure of objects in the RSM database.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

Size of the information structure, in bytes. This member must be set to the correct size of the structure prior to using either the 
<a href="https://msdn.microsoft.com/e5c1b165-2c55-40c3-94d8-c996c5db4250">GetNtmsObjectInformation</a>
			function or the 
<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a> function.


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
<a href="https://msdn.microsoft.com/2aa9fccf-dea3-4fa3-9fbf-6d83770c3893">NTMS_CHANGERINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_CHANGER_TYPE"></a><a id="ntms_changer_type"></a><dl>
<dt><b>NTMS_CHANGER_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A changer type object is created for each unique changer device type attached to a system. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/49c219d7-5772-4868-80dd-ab1e1f1471b1">NTMS_CHANGERTYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_COMPUTER"></a><a id="ntms_computer"></a><dl>
<dt><b>NTMS_COMPUTER</b></dt>
</dl>
</td>
<td width="60%">
The current computer object. There is no structure for the computer object. The <b>Info</b> member is a pointer to an <a href="https://msdn.microsoft.com/11dd71eb-7193-40d5-b193-4d529eec3ca7">NTMS_COMPUTERINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE"></a><a id="ntms_drive"></a><dl>
<dt><b>NTMS_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
A drive object represents a tape drive or disk drive. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/a095a8f1-a059-4aed-88da-a139286993b5">NTMS_DRIVEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE_TYPE"></a><a id="ntms_drive_type"></a><dl>
<dt><b>NTMS_DRIVE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A drive type object is created for each unique drive device type attached to a system. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/2c852397-540c-44f9-a94e-2100d1588d75">NTMS_DRIVETYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEDOOR"></a><a id="ntms_iedoor"></a><dl>
<dt><b>NTMS_IEDOOR</b></dt>
</dl>
</td>
<td width="60%">
An NTMS_IEDOOR object represents the door-access mechanism of a library unit. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/a0619420-f391-4695-a87e-8cbf8d3a3742">NTMS_IEDOORINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEPORT"></a><a id="ntms_ieport"></a><dl>
<dt><b>NTMS_IEPORT</b></dt>
</dl>
</td>
<td width="60%">
An NTMS_IEPORT object represents the insert/eject port of a library unit. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/e932a482-12d8-4fb2-bbbc-0e0cf6ee0b42">NTMS_IEPORTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
A library object represents an online or offline library. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/f8ca33ba-35e2-4fd9-a9a0-1393bbbede80">NTMS_LIBRARYINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQUEST"></a><a id="ntms_librequest"></a><dl>
<dt><b>NTMS_LIBREQUEST</b></dt>
</dl>
</td>
<td width="60%">
A library request object is created for each request for a library to perform an action. A list of library requests is maintained by RSM as a queue of work to be performed. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/0250ed88-410c-4fe3-8188-5e6253d45dc4">NTMS_LIBREQUESTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LOGICAL_MEDIA"></a><a id="ntms_logical_media"></a><dl>
<dt><b>NTMS_LOGICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The primary handle used by applications to access the specified medium. In the case of multi-sided media, each side is treated as an individual piece of physical media. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/f1a003af-101a-4f1f-b644-392e5542e8dd">NTMS_LMIDINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_POOL"></a><a id="ntms_media_pool"></a><dl>
<dt><b>NTMS_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
A media pool is a logical grouping of media. All media in a media pool must be the same media type. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/4feb9d68-f88b-4515-9c59-64fe9c5594d6">NTMS_MEDIAPOOLINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIA_TYPE"></a><a id="ntms_media_type"></a><dl>
<dt><b>NTMS_MEDIA_TYPE</b></dt>
</dl>
</td>
<td width="60%">
A media type object is created for each unique media type in a system. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/38020a77-0340-4096-a2a8-d16eec5857e6">NTMS_MEDIATYPEINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQUEST"></a><a id="ntms_oprequest"></a><dl>
<dt><b>NTMS_OPREQUEST</b></dt>
</dl>
</td>
<td width="60%">
An operator request object represents an RSM request for a user to get the information. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/d6ff9240-8f58-4f2e-9298-ff2f0193eeba">NTMS_OPREQUESTINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTITION"></a><a id="ntms_partition"></a><dl>
<dt><b>NTMS_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
A side object represents a side of a piece of physical media. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/75ba3b8d-4b44-49be-b238-e02e62c3def6">NTMS_PARTITIONINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PHYSICAL_MEDIA"></a><a id="ntms_physical_media"></a><dl>
<dt><b>NTMS_PHYSICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
A physical media object represents a magnetic tape or removable disk. A piece of physical media can contain one or more sides. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/9ed46cc9-0b93-44ef-9c33-1e1baadb225f">NTMS_PMIDINFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_STORAGESLOT"></a><a id="ntms_storageslot"></a><dl>
<dt><b>NTMS_STORAGESLOT</b></dt>
</dl>
</td>
<td width="60%">
A storage slot object represents one of the slots that can hold the specified medium in a library. The <b>Info</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/95b9d2e9-ddf3-459f-b9de-cefc15adb419">NTMS_STORAGESLOTINFORMATION</a> structure.

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
<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a> function. All other object names are read-only.


### -field szDescription

Type: <b>TCHAR[NTMS_DESCRIPTION_LENGTH]</b>

Description of the device or system control object. The description of device and system control objects can be changed using the 
<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a> function. (Writable for all objects)


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

 


### -field Info.switch_is

 


### -field Info.switch_is.dwType

 


### -field Info

Device or system control object-specific information. The format of this information depends on the <b>dwType</b> member.


### -field Info.Drive

<b>Type: <b><a href="https://msdn.microsoft.com/a095a8f1-a059-4aed-88da-a139286993b5">NTMS_DRIVEINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_DRIVE</b>.


### -field Info.DriveType

<b>Type: <b><a href="https://msdn.microsoft.com/2c852397-540c-44f9-a94e-2100d1588d75">NTMS_DRIVETYPEINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_DRIVE_TYPE</b>.


### -field Info.Library

<b>Type: <b><a href="https://msdn.microsoft.com/f8ca33ba-35e2-4fd9-a9a0-1393bbbede80">NTMS_LIBRARYINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_LIBRARY</b>.


### -field Info.Changer

<b>Type: <b><a href="https://msdn.microsoft.com/2aa9fccf-dea3-4fa3-9fbf-6d83770c3893">NTMS_CHANGERINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_CHANGER</b>.


### -field Info.ChangerType

<b>Type: <b><a href="https://msdn.microsoft.com/49c219d7-5772-4868-80dd-ab1e1f1471b1">NTMS_CHANGERTYPEINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_CHANGER_TYPE</b>.


### -field Info.StorageSlot

<b>Type: <b><a href="https://msdn.microsoft.com/95b9d2e9-ddf3-459f-b9de-cefc15adb419">NTMS_STORAGESLOTINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_STORAGESLOT</b>.


### -field Info.IEDoor

<b>Type: <b><a href="https://msdn.microsoft.com/a0619420-f391-4695-a87e-8cbf8d3a3742">NTMS_IEDOORINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_IEDOOR</b>.


### -field Info.IEPort

<b>Type: <b><a href="https://msdn.microsoft.com/e932a482-12d8-4fb2-bbbc-0e0cf6ee0b42">NTMS_IEPORTINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_IEPORT</b>.


### -field Info.PhysicalMedia

<b>Type: <b><a href="https://msdn.microsoft.com/9ed46cc9-0b93-44ef-9c33-1e1baadb225f">NTMS_PMIDINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_PHYSICAL_MEDIA</b>.


### -field Info.LogicalMedia

<b>Type: <b><a href="https://msdn.microsoft.com/f1a003af-101a-4f1f-b644-392e5542e8dd">NTMS_LMIDINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_LOGICAL_MEDIA</b>.


### -field Info.Partition

<b>Type: <b><a href="https://msdn.microsoft.com/75ba3b8d-4b44-49be-b238-e02e62c3def6">NTMS_PARTITIONINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_PARTITION</b>.


### -field Info.MediaPool

<b>Type: <b><a href="https://msdn.microsoft.com/4feb9d68-f88b-4515-9c59-64fe9c5594d6">NTMS_MEDIAPOOLINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_MEDIA_POOL</b>.


### -field Info.MediaType

<b>Type: <b><a href="https://msdn.microsoft.com/38020a77-0340-4096-a2a8-d16eec5857e6">NTMS_MEDIATYPEINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_MEDIA_TYPE</b>.


### -field Info.LibRequest

<b>Type: <b><a href="https://msdn.microsoft.com/0250ed88-410c-4fe3-8188-5e6253d45dc4">NTMS_LIBREQUESTINFORMATION</a></b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_LIBREQUEST</b>.


### -field Info.OpRequest

<b>Type: <b>NTMS_OPREQUESTINFORMATION</b>
</b>
This format is used if the <b>dwType</b> value is <b>NTMS_OPREQUEST</b>.


### -field Info.Computer

 




## -remarks



All members of the 
<b>NTMS_OBJECTINFORMATION</b> structure are read-only at the RSM function-level unless specified as WRITABLE in the definition of the member.




## -see-also




<a href="https://msdn.microsoft.com/e5c1b165-2c55-40c3-94d8-c996c5db4250">GetNtmsObjectInformation</a>



<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a>
 

 

