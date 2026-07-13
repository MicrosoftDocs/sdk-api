---
UID: NF:ntmsapi.CreateNtmsMediaW
title: CreateNtmsMediaW function (ntmsapi.h)
description: The CreateNtmsMedia function creates a PMID and side (or sides) for a new piece of offline media. The media is placed in the media pool specified for lpPhysicalMedia. (Unicode)
helpviewer_keywords: ["CreateNtmsMedia", "CreateNtmsMedia function [Files]", "CreateNtmsMediaW", "NTMS_ERROR_ON_DUPLICATE", "_zaw_createntmsmedia", "base.createntmsmedia", "fs.createntmsmedia", "ntmsapi/CreateNtmsMedia", "ntmsapi/CreateNtmsMediaW"]
old-location: fs\createntmsmedia.htm
tech.root: fs
ms.assetid: a44c51c3-13d7-490e-9b6f-4d4c82d5a8f8
ms.date: 12/05/2018
ms.keywords: CreateNtmsMedia, CreateNtmsMedia function [Files], CreateNtmsMediaA, CreateNtmsMediaW, NTMS_ERROR_ON_DUPLICATE, _zaw_createntmsmedia, base.createntmsmedia, fs.createntmsmedia, ntmsapi/CreateNtmsMedia, ntmsapi/CreateNtmsMediaA, ntmsapi/CreateNtmsMediaW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateNtmsMediaW (Unicode) and CreateNtmsMediaA (ANSI)
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
 - CreateNtmsMediaW
 - ntmsapi/CreateNtmsMediaW
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
 - CreateNtmsMedia
 - CreateNtmsMediaA
 - CreateNtmsMediaW
---

# CreateNtmsMediaW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CreateNtmsMedia</b> function creates a PMID and side (or sides) for a new piece of offline media. The media is placed in the media pool specified for <i>lpPhysicalMedia</i>.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMedia [in]

Pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure that contains information about the medium to create. For a description of the applicable members, see Remarks.

### -param lpList [in]

Pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure that specifies array of sides associated with the medium. For a description of the applicable members, see Remarks.

### -param dwOptions [in]

Options. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Default value. Allows the creation of a duplicate medium with a duplicate OMID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_ERROR_ON_DUPLICATE"></a><a id="ntms_error_on_duplicate"></a><dl>
<dt><b>NTMS_ERROR_ON_DUPLICATE</b></dt>
</dl>
</td>
<td width="60%">
Returns an error and does not create the medium if a medium with the specified OMID already exists on the system.

</td>
</tr>
</table>

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
NTMS_MODIFY_ACCESS to the computer or the media's media pool is denied. Other security errors are possible, but indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the media pool or NTMS_MODIFY_ACCESS to the offline library is denied. Other security errors are possible, but indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Database inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_OMID</b></dt>
</dl>
</td>
<td width="60%">
The option NTMS_ERROR_ON_DUPLICATE was provided and a medium already exists with this OMID.

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
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
An entry already exists for a medium with this barcode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
Media pool specified either does not exist, or is not a valid Import or Application pool.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is missing, or the object information size or object type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
Number of specified sides does not match the number of sides associated with the media pool's media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function executed successfully.

</td>
</tr>
</table>

## -remarks

The <i>lpMedia</i> parameter must point to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure, whose <b>dwType</b> parameter is NTMS_PHYSICAL_MEDIA. The following is a list of members and descriptions for the 
<b>NTMS_OBJECTINFORMATION</b> structure.

<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>[in] 
<b>CreateNtmsMedia</b> verifies that this size equals the length of an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure containing an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_pmidinformationa">NTMS_PMIDINFORMATION</a> structure. It returns ERROR_INVALID_PARAMETER if the size is incorrect.</td>
</tr>
<tr>
<td><b>dwType</b></td>
<td>[in] 
<b>CreateNtmsMedia</b> verifies that the value NTMS_PHYSICAL_MEDIA was provided. It returns ERROR_INVALID_PARAMETER if the provided type is incorrect.</td>
</tr>
<tr>
<td><b>Created</b></td>
<td>[out] Indicates time the physical media object was entered into the NTMS database.</td>
</tr>
<tr>
<td><b>Modified</b></td>
<td>[out] Indicates time the physical media object was entered into the NTMS database.</td>
</tr>
<tr>
<td><b>ObjectGuid</b></td>
<td>[in/out] Unique identifier for the physical media object (PMID). If a non-<b>NULL</b> value is provided, the value is used as the GUID of the Physical Medium, otherwise a GUID is generated.</td>
</tr>
<tr>
<td><b>Enabled</b></td>
<td>[in] Indicates whether or not the physical medium should be enabled.</td>
</tr>
<tr>
<td><b>dwOperationalState</b></td>
<td>[out] Must be NTMS_READY.</td>
</tr>
<tr>
<td><b>szName</b></td>
<td>[in/out] 
<b>CreateNtmsMedia</b> allows an application to specify the name of a new physical medium. This enables the application to continue to use the name of a medium after moving it from one RSM computer to another. The RSM default naming selection is: for single sided: Barcode, then Label Info value or Sequence Number;. for multi-sided media Barcode then Sequence Number. 


Note that the name that appears in the RSM user interface for a partition is this name (the name assigned to the physical media object).

</td>
</tr>
<tr>
<td><b>szDescription</b></td>
<td>[in] An optional parameter that may be set using 
<b>CreateNtmsMedia</b>. Provide the empty string ("\0") to avoid passing in a value for the description.</td>
</tr>
</table>
 

The following is a list of members and descriptions for the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_pmidinformationa">NTMS_PMIDINFORMATION</a> structure.

<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td><b>CurrentLibrary</b></td>
<td>[in] Must be either the NULL_GUID, or the GUID of the Offline library.</td>
</tr>
<tr>
<td><b>MediaPool</b></td>
<td>[in] Must be the GUID of a valid Import or Application pool. 


<b>CreateNtmsMedia</b> verifies that this is the GUID of a valid Import or Application Pool. It also verifies that the number of partitions provided are correct for the media type associated with this media pool.

</td>
</tr>
<tr>
<td><b>Location</b></td>
<td>[out] Must be the NULL_GUID.</td>
</tr>
<tr>
<td><b>LocationType</b></td>
<td>[out] Must be NTMS_STORAGESLOT.</td>
</tr>
<tr>
<td><b>HomeSlot</b></td>
<td>[out] Must be the NULL_GUID.</td>
</tr>
<tr>
<td><b>MediaType</b></td>
<td>[out] 
<b>CreateNtmsMedia</b> sets the media type to the media type associated with the media pool provided.</td>
</tr>
<tr>
<td><b>szBarCode</b></td>
<td>[in/out] The barcode is stripped of any ending spaces. 
<b>CreateNtmsMedia</b> does not perform any additional attempts at verifying the validity of the barcode.</td>
</tr>
<tr>
<td><b>BarCodeState</b></td>
<td>[out] The <b>BarCodeState</b> is set to NTMS_BARCODESTATE_UNREADABLE if the value passed in for <b>szBarCode</b> is an empty string, otherwise it is set to NTMS_BARCODESTATE_OK.</td>
</tr>
<tr>
<td><b>szSequenceNumber</b></td>
<td>[out] 
<b>CreateNtmsMedia</b> assigns the newly-created medium a sequence number, which is returned in this member.</td>
</tr>
<tr>
<td><b>MediaState</b></td>
<td>[out] 
<b>CreateNtmsMedia</b> sets the MediaState to NTMS_MEDIASTATE_IDLE.</td>
</tr>
<tr>
<td><b>dwNumberOfPartitions</b></td>
<td>[in] Defines the number of 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structures representing sides for this medium. 
<b>CreateNtmsMedia</b> checks to ensure that the number of sides specified matches the number of sides implied by the media pool to which it is to be assigned. If they do not match, ERROR_MEDIA_INCOMPATIBLE is returned.</td>
</tr>
<tr>
<td><b>dwMediaTypeCode</b></td>
<td>[in] SCSI media type code. 


This member is not used by RSM, but may be used by applications written to RSM for additional information about the media. For a description of what this member should be set to, see the Hardware Manufacturer's SCSI spec for possible settings.

RSM updates this member when it mounts the newly-imported medium for the first time.

</td>
</tr>
<tr>
<td><b>dwDensityCode</b></td>
<td>[in] SCSI density code. 


This member is not used by RSM, but may be used by applications written to RSM for additional information about the media. For a description of what this member should be set to, see the Hardware Manufacturer's SCSI spec for possible settings.

RSM updates this member when it mounts the newly-imported medium for the first time

</td>
</tr>
</table>
 

The <i>lpList</i> parameter must point to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure whose <b>dwType</b> is NTMS_PARTITION with the following information.

<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>[in] 
<b>CreateNtmsMedia</b> verifies that the provided size matches the expected length of an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure containing an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_partitioninformationa">NTMS_PARTITIONINFORMATION</a> structure. It returns ERROR_INVALID_PARAMETER if the size is incorrect.</td>
</tr>
<tr>
<td><b>dwType</b></td>
<td>[in] 
<b>CreateNtmsMedia</b> verifies that the value NTMS_PARTITION was provided. It returns ERROR_INVALID_PARAMETER if the provided type is incorrect.</td>
</tr>
<tr>
<td><b>Created</b></td>
<td>[out] Indicates the time that the partition object was entered into the RSM database.</td>
</tr>
<tr>
<td><b>Modified</b></td>
<td>[out] Indicates the time that the partition object was entered into the RSM database.</td>
</tr>
<tr>
<td><b>ObjectGuid</b></td>
<td>[in/out] Unique identifier for the side. If a non-<b>NULL</b> value is provided, the value is used as the GUID of the side; otherwise, a GUID is generated.</td>
</tr>
<tr>
<td><b>Enabled</b></td>
<td>[in] Determines whether or not the side should be enabled.</td>
</tr>
<tr>
<td><b>dwOperationalState</b></td>
<td>[out] Must be NTMS_READY.</td>
</tr>
<tr>
<td><b>szName</b></td>
<td>[in] Name of a new side.</td>
</tr>
<tr>
<td><b>szDescription</b></td>
<td>[in] Optional parameter that may be set using 
<b>CreateNtmsMedia</b>. Provide the empty string ("\0") to avoid passing in a value for the description.</td>
</tr>
<tr>
<td><b>PhysicalMedia</b></td>
<td>[out] GUID of the newly-created side object.</td>
</tr>
<tr>
<td><b>LogicalMedia</b></td>
<td>[in/out] Optional input parameter, as well as an output parameter. If the GUID is provided, 
<b>CreateNtmsMedia</b> attempts to create a new logical media object with the preassigned GUID. If the GUID is not unique, 
<b>CreateNtmsMedia</b> returns an error.</td>
</tr>
<tr>
<td><b>State</b></td>
<td>[in] Any valid side state.</td>
</tr>
<tr>
<td><b>Side</b></td>
<td>[out] 
<b>CreateNtmsMedia</b> sets the side number to its offset in the Partitions array.</td>
</tr>
<tr>
<td><b>dwOmidLabelIdLength</b></td>
<td>[in] Must be a positive value. 


<b>CreateNtmsMedia</b> uses the <b>dwOmidLabelIdLength</b> to determine the number of significant bytes in the <b>OmidLabelId</b> member. If the value is not correct, the recorded <b>OmidLabelId</b> is incorrect.

</td>
</tr>
<tr>
<td><b>OmidLabelId</b></td>
<td>[in] Must be a valid media label that can be recognized by an installed MLL.</td>
</tr>
<tr>
<td><b>szOmidLabelType</b></td>
<td>[in] Must not be an empty string.</td>
</tr>
<tr>
<td><b>szOmidLabelInfo</b></td>
<td>[in] May be the empty string.</td>
</tr>
<tr>
<td><b>dwMountCount</b></td>
<td>[in] Any value is accepted.</td>
</tr>
<tr>
<td><b>dwAllocateCount</b></td>
<td>[in] Any value is accepted.</td>
</tr>
<tr>
<td><b>Capacity</b></td>
<td>[in] SCSI capacity code. 


This member is not used by RSM, but may be used by applications written to RSM for additional information about the media. For a description of what this member should be set to, see the Hardware Manufacturer's SCSI spec for possible settings.

RSM updates this member when it mounts the newly-imported medium for the first time.

</td>
</tr>
</table>
 





> [!NOTE]
> The ntmsapi.h header defines CreateNtmsMedia as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>
