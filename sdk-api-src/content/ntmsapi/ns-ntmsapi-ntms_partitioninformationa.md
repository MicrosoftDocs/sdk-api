---
UID: NS:ntmsapi._NTMS_PARTITIONINFORMATIONA
title: NTMS_PARTITIONINFORMATIONA (ntmsapi.h)
description: The NTMS_PARTITIONINFORMATION structure defines the properties specific to the side object. (ANSI)
helpviewer_keywords: ["NTMS_PARTITIONINFORMATION","NTMS_PARTITIONINFORMATION structure [Files]","NTMS_PARTITIONINFORMATIONA","NTMS_PARTITIONINFORMATIONW","NTMS_PARTSTATE_ALLOCATED","NTMS_PARTSTATE_AVAILABLE","NTMS_PARTSTATE_COMPLETE","NTMS_PARTSTATE_DECOMMISIONED","NTMS_PARTSTATE_FOREIGN","NTMS_PARTSTATE_IMPORT","NTMS_PARTSTATE_INCOMPATIBLE","NTMS_PARTSTATE_RESERVED","NTMS_PARTSTATE_UNPREPARED","_NTMS_PARTITIONINFORMATIONA","_NTMS_PARTITIONINFORMATIONW","_zaw_ntms_partitioninformation","base.ntms_partitioninformation","fs.ntms_partitioninformation","ntmsapi/NTMS_PARTITIONINFORMATION"]
old-location: fs\ntms_partitioninformation.htm
tech.root: fs
ms.assetid: 75ba3b8d-4b44-49be-b238-e02e62c3def6
ms.date: 12/05/2018
ms.keywords: NTMS_PARTITIONINFORMATION, NTMS_PARTITIONINFORMATION structure [Files], NTMS_PARTITIONINFORMATIONA, NTMS_PARTITIONINFORMATIONW, NTMS_PARTSTATE_ALLOCATED, NTMS_PARTSTATE_AVAILABLE, NTMS_PARTSTATE_COMPLETE, NTMS_PARTSTATE_DECOMMISIONED, NTMS_PARTSTATE_FOREIGN, NTMS_PARTSTATE_IMPORT, NTMS_PARTSTATE_INCOMPATIBLE, NTMS_PARTSTATE_RESERVED, NTMS_PARTSTATE_UNPREPARED, _NTMS_PARTITIONINFORMATIONA, _NTMS_PARTITIONINFORMATIONW, _zaw_ntms_partitioninformation, base.ntms_partitioninformation, fs.ntms_partitioninformation, ntmsapi/NTMS_PARTITIONINFORMATION
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
req.typenames: NTMS_PARTITIONINFORMATIONA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_PARTITIONINFORMATIONA
 - ntmsapi/_NTMS_PARTITIONINFORMATIONA
 - NTMS_PARTITIONINFORMATIONA
 - ntmsapi/NTMS_PARTITIONINFORMATIONA
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
 - NTMS_PARTITIONINFORMATION
 - NTMS_PARTITIONINFORMATIONA
 - NTMS_PARTITIONINFORMATIONW
---

# NTMS_PARTITIONINFORMATIONA structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_PARTITIONINFORMATION</b> structure defines the properties specific to the side object.

## -struct-fields

### -field PhysicalMedia

Unique physical media identifier for the medium that contains this side.

### -field LogicalMedia

Unique logical media identifier (LMID) for a piece of logical media that contains this side. This parameter is a <b>NULL</b> if the side is not allocated.

### -field State

Side life cycle information. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_ALLOCATED"></a><a id="ntms_partstate_allocated"></a><dl>
<dt><b>NTMS_PARTSTATE_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
The media has been allocated to an application.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_AVAILABLE"></a><a id="ntms_partstate_available"></a><dl>
<dt><b>NTMS_PARTSTATE_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The media is available to be allocated.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_COMPLETE"></a><a id="ntms_partstate_complete"></a><dl>
<dt><b>NTMS_PARTSTATE_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The media has been completely written and marked as complete by an application.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_DECOMMISIONED"></a><a id="ntms_partstate_decommisioned"></a><dl>
<dt><b>NTMS_PARTSTATE_DECOMMISIONED</b></dt>
</dl>
</td>
<td width="60%">
The media is unsuitable for data storage and is no longer usable.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_INCOMPATIBLE"></a><a id="ntms_partstate_incompatible"></a><dl>
<dt><b>NTMS_PARTSTATE_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
The media has been found to be and marked as incompatible with the drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_FOREIGN"></a><a id="ntms_partstate_foreign"></a><dl>
<dt><b>NTMS_PARTSTATE_FOREIGN</b></dt>
</dl>
</td>
<td width="60%">
The media is in a unrecognized pool.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_IMPORT"></a><a id="ntms_partstate_import"></a><dl>
<dt><b>NTMS_PARTSTATE_IMPORT</b></dt>
</dl>
</td>
<td width="60%">
The media is in the import pool.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_UNPREPARED"></a><a id="ntms_partstate_unprepared"></a><dl>
<dt><b>NTMS_PARTSTATE_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The media is waiting for a free label to be applied.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTSTATE_RESERVED"></a><a id="ntms_partstate_reserved"></a><dl>
<dt><b>NTMS_PARTSTATE_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
The side has been reserved by the 
<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a> function with the <i>dwOption</i> parameter set to NTMS_ALLOCATE_NEW.

</td>
</tr>
</table>

### -field Side

Zero-relative value which indicates which side of a multi-sided media this is. For single-sided media, such as tape, this value is always zero. For dual-sided media one NTMS_PARITIONINFORMATION record has this property set to zero - the "A" side - and a second NTMS_PARTITIONINFORMATION record has it set to 1 - the "B" side.

### -field dwOmidLabelIdLength

Length of the label ID string of the on-media identifier.

### -field OmidLabelId

Label ID unique identifier of the on-media identifier.

### -field szOmidLabelType

Label type of the on-media identifier.

### -field szOmidLabelInfo

Label information of the on-media identifier.

### -field dwMountCount

Number of times this media has been mounted into a drive. This is initialized to zero when the objects are created in the database.

### -field dwAllocateCount

Number of times this media has been allocated.

### -field Capacity

Number bytes of storage available on this side.

## -remarks

The 
<b>NTMS_PARTITIONINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_PARTITIONINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
