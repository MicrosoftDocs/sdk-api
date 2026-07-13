---
UID: NS:ntmsapi._NTMS_PMIDINFORMATIONW
title: NTMS_PMIDINFORMATIONW (ntmsapi.h)
description: The NTMS_PMIDINFORMATION structure defines the properties specific to a physical media object. (Unicode)
helpviewer_keywords: ["NTMS_BARCODESTATE_OK","NTMS_BARCODESTATE_UNREADABLE","NTMS_MEDIASTATE_IDLE","NTMS_MEDIASTATE_INUSE","NTMS_MEDIASTATE_LOADED","NTMS_MEDIASTATE_MOUNTED","NTMS_MEDIASTATE_OPREQ","NTMS_MEDIASTATE_OP_ERROR","NTMS_MEDIASTATE_UNLOADED","NTMS_PMIDINFORMATION","NTMS_PMIDINFORMATION structure [Files]","NTMS_PMIDINFORMATIONA","NTMS_PMIDINFORMATIONW","_NTMS_PMIDINFORMATIONA","_NTMS_PMIDINFORMATIONW","_zaw_ntms_pmidinformation","base.ntms_pmidinformation","fs.ntms_pmidinformation","ntmsapi/NTMS_PMIDINFORMATION"]
old-location: fs\ntms_pmidinformation.htm
tech.root: fs
ms.assetid: 9ed46cc9-0b93-44ef-9c33-1e1baadb225f
ms.date: 12/05/2018
ms.keywords: NTMS_BARCODESTATE_OK, NTMS_BARCODESTATE_UNREADABLE, NTMS_MEDIASTATE_IDLE, NTMS_MEDIASTATE_INUSE, NTMS_MEDIASTATE_LOADED, NTMS_MEDIASTATE_MOUNTED, NTMS_MEDIASTATE_OPREQ, NTMS_MEDIASTATE_OP_ERROR, NTMS_MEDIASTATE_UNLOADED, NTMS_PMIDINFORMATION, NTMS_PMIDINFORMATION structure [Files], NTMS_PMIDINFORMATIONA, NTMS_PMIDINFORMATIONW, _NTMS_PMIDINFORMATIONA, _NTMS_PMIDINFORMATIONW, _zaw_ntms_pmidinformation, base.ntms_pmidinformation, fs.ntms_pmidinformation, ntmsapi/NTMS_PMIDINFORMATION
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
req.typenames: NTMS_PMIDINFORMATIONW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_PMIDINFORMATIONW
 - ntmsapi/_NTMS_PMIDINFORMATIONW
 - NTMS_PMIDINFORMATIONW
 - ntmsapi/NTMS_PMIDINFORMATIONW
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
 - NTMS_PMIDINFORMATION
 - NTMS_PMIDINFORMATIONA
 - NTMS_PMIDINFORMATIONW
---

# NTMS_PMIDINFORMATIONW structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_PMIDINFORMATION</b> structure defines the properties specific to a physical media object.

## -struct-fields

### -field CurrentLibrary

Unique ID of the library in which the media is contained.

### -field MediaPool

Unique ID of the media pool to which the media is assigned.

### -field Location

Unique ID of the physical location object for the media.

### -field LocationType

Current location type of a piece of physical media. The value of this member can be set to NTMS_STORAGESLOT, NTMS_DRIVE, NTMS_IEPORT. (Offline media are in slots.)

### -field MediaType

Unique ID of a media type object.

### -field HomeSlot

Unique ID of the library storage slot in which media is stored.

### -field szBarCode

String that matches the bar-code value on a bar-code label of a piece of physical media.

### -field BarCodeState

Current state of the bar code. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_BARCODESTATE_OK"></a><a id="ntms_barcodestate_ok"></a><dl>
<dt><b>NTMS_BARCODESTATE_OK</b></dt>
</dl>
</td>
<td width="60%">
The media has a bar code and it is readable.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_BARCODESTATE_UNREADABLE"></a><a id="ntms_barcodestate_unreadable"></a><dl>
<dt><b>NTMS_BARCODESTATE_UNREADABLE</b></dt>
</dl>
</td>
<td width="60%">
The media either does not have a bar code or the bar code is unreadable.

</td>
</tr>
</table>

### -field szSequenceNumber

Sequential number assigned to the specified medium as a human-readable value that must be transcribed by a user on the medium so that the medium can be located in an offline library.

### -field MediaState

Current state for the piece of physical media. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_IDLE"></a><a id="ntms_mediastate_idle"></a><dl>
<dt><b>NTMS_MEDIASTATE_IDLE</b></dt>
</dl>
</td>
<td width="60%">
The media is in a slot in the library, in a drive dismounted, or in an offline library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_INUSE"></a><a id="ntms_mediastate_inuse"></a><dl>
<dt><b>NTMS_MEDIASTATE_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The media is marked as in use as soon as a request for an operation is successfully made to RSM.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_LOADED"></a><a id="ntms_mediastate_loaded"></a><dl>
<dt><b>NTMS_MEDIASTATE_LOADED</b></dt>
</dl>
</td>
<td width="60%">
The state of the media when RSM has determined that the media is available for reading and writing.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_MOUNTED"></a><a id="ntms_mediastate_mounted"></a><dl>
<dt><b>NTMS_MEDIASTATE_MOUNTED</b></dt>
</dl>
</td>
<td width="60%">
The state of a piece of physical media when the media is placed in a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_OP_ERROR"></a><a id="ntms_mediastate_op_error"></a><dl>
<dt><b>NTMS_MEDIASTATE_OP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The physical media is in an error state that is recoverable. No operator intervention is required.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_UNLOADED"></a><a id="ntms_mediastate_unloaded"></a><dl>
<dt><b>NTMS_MEDIASTATE_UNLOADED</b></dt>
</dl>
</td>
<td width="60%">
The state of the media when it is ready to be removed from a drive. The drive state, DISMOUNTABLE, also indicates that a drive can be removed at any time.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIASTATE_OPREQ"></a><a id="ntms_mediastate_opreq"></a><dl>
<dt><b>NTMS_MEDIASTATE_OPREQ</b></dt>
</dl>
</td>
<td width="60%">
Media is waiting for operator request.

</td>
</tr>
</table>

### -field dwNumberOfPartitions

Number of sides on the medium.

### -field dwMediaTypeCode

SCSI media type code.

### -field dwDensityCode

SCSI density code.

### -field MountedPartition

Globally unique ID of the side of the media that is currently mounted.

## -remarks

The 
<b>NTMS_PMIDINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_PMIDINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
