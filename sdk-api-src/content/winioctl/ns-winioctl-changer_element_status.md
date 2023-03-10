---
UID: NS:winioctl._CHANGER_ELEMENT_STATUS
title: CHANGER_ELEMENT_STATUS
description: Represents the status of the specified element. (CHANGER_ELEMENT_STATUS)
helpviewer_keywords: ["*PCHANGER_ELEMENT_STATUS","CHANGER_ELEMENT_STATUS","CHANGER_ELEMENT_STATUS structure","ELEMENT_STATUS_ACCESS","ELEMENT_STATUS_AVOLTAG","ELEMENT_STATUS_EXCEPT","ELEMENT_STATUS_EXENAB","ELEMENT_STATUS_FULL","ELEMENT_STATUS_ID_VALID","ELEMENT_STATUS_IMPEXP","ELEMENT_STATUS_INENAB","ELEMENT_STATUS_INVERT","ELEMENT_STATUS_LUN_VALID","ELEMENT_STATUS_NOT_BUS","ELEMENT_STATUS_PVOLTAG","ELEMENT_STATUS_SVALID","ERROR_DRIVE_NOT_INSTALLED","ERROR_LABEL_QUESTIONABLE","ERROR_LABEL_UNREADABLE","ERROR_SLOT_NOT_PRESENT","ERROR_TRAY_MALFUNCTION","ERROR_UNHANDLED_ERROR","PCHANGER_ELEMENT_STATUS","PCHANGER_ELEMENT_STATUS structure pointer","_win32_changer_element_status_str","base.changer_element_status_str","winioctl/CHANGER_ELEMENT_STATUS","winioctl/PCHANGER_ELEMENT_STATUS"]
old-location: base\changer_element_status_str.htm
tech.root: base
ms.assetid: 9714994f-4923-48bf-8f96-6a960a87bd5f
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_ELEMENT_STATUS, CHANGER_ELEMENT_STATUS, CHANGER_ELEMENT_STATUS structure, ELEMENT_STATUS_ACCESS, ELEMENT_STATUS_AVOLTAG, ELEMENT_STATUS_EXCEPT, ELEMENT_STATUS_EXENAB, ELEMENT_STATUS_FULL, ELEMENT_STATUS_ID_VALID, ELEMENT_STATUS_IMPEXP, ELEMENT_STATUS_INENAB, ELEMENT_STATUS_INVERT, ELEMENT_STATUS_LUN_VALID, ELEMENT_STATUS_NOT_BUS, ELEMENT_STATUS_PVOLTAG, ELEMENT_STATUS_SVALID, ERROR_DRIVE_NOT_INSTALLED, ERROR_LABEL_QUESTIONABLE, ERROR_LABEL_UNREADABLE, ERROR_SLOT_NOT_PRESENT, ERROR_TRAY_MALFUNCTION, ERROR_UNHANDLED_ERROR, PCHANGER_ELEMENT_STATUS, PCHANGER_ELEMENT_STATUS structure pointer, _win32_changer_element_status_str, base.changer_element_status_str, winioctl/CHANGER_ELEMENT_STATUS, winioctl/PCHANGER_ELEMENT_STATUS'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CHANGER_ELEMENT_STATUS, *PCHANGER_ELEMENT_STATUS
req.redist: 
f1_keywords:
 - _CHANGER_ELEMENT_STATUS
 - winioctl/_CHANGER_ELEMENT_STATUS
 - PCHANGER_ELEMENT_STATUS
 - winioctl/PCHANGER_ELEMENT_STATUS
 - CHANGER_ELEMENT_STATUS
 - winioctl/CHANGER_ELEMENT_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_ELEMENT_STATUS
---

# CHANGER_ELEMENT_STATUS structure


## -description

Represents the status of the specified element.

## -struct-fields

### -field Element

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that represents the element.

### -field SrcElementAddress

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that represents the element from which the media currently in this element was most recently moved.

This member is valid only if the <b>Flags</b> member includes ELEMENT_STATUS_SVALID.

### -field Flags

The element status. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_ACCESS"></a><a id="element_status_access"></a><dl>
<dt><b>ELEMENT_STATUS_ACCESS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The changer's transport element can access the piece of media in this element. The media is not accessible in the following circumstances: (1) If the element type is ChangerSlot, the slot is not present in the changer (for example, the magazine containing the slot has been physically removed). (2) If the element type is ChangerDrive, the drive is broken or has been removed. (3) If the element type is ChangerIEPort, the changer's insert/eject port is extended.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_AVOLTAG"></a><a id="element_status_avoltag"></a><dl>
<dt><b>ELEMENT_STATUS_AVOLTAG</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Alternate volume information in the <b>AlternateVolumeID</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_EXCEPT"></a><a id="element_status_except"></a><dl>
<dt><b>ELEMENT_STATUS_EXCEPT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The element is in an abnormal state. Check the <b>ExceptionCode</b> member for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_EXENAB"></a><a id="element_status_exenab"></a><dl>
<dt><b>ELEMENT_STATUS_EXENAB</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The element supports export of media through the changer's insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_FULL"></a><a id="element_status_full"></a><dl>
<dt><b>ELEMENT_STATUS_FULL</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The element contains a piece of media. 




Note that this value is valid only if the element type is ChangerDrive, ChangerSlot, or ChangerTransport. If <b>ElementType</b> is ChangerIEPort, this value is valid only if the <b>Features0</b> member of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a> includes CHANGER_REPORT_IEPORT_STATE.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_ID_VALID"></a><a id="element_status_id_valid"></a><dl>
<dt><b>ELEMENT_STATUS_ID_VALID</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The SCSI target ID in the <b>TargetID</b> member is valid. 




This value is valid only if the element type is ChangerDrive.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_IMPEXP"></a><a id="element_status_impexp"></a><dl>
<dt><b>ELEMENT_STATUS_IMPEXP</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The media in this element was placed there by an operator. 




This value is valid only if the element type is ChangerIEPort.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_INENAB"></a><a id="element_status_inenab"></a><dl>
<dt><b>ELEMENT_STATUS_INENAB</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The element supports import of media through the changer's insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_INVERT"></a><a id="element_status_invert"></a><dl>
<dt><b>ELEMENT_STATUS_INVERT</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
The media in the element was flipped. 




This value is valid only if ELEMENT_STATUS_SVALID is also included.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_LUN_VALID"></a><a id="element_status_lun_valid"></a><dl>
<dt><b>ELEMENT_STATUS_LUN_VALID</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The logical unit number in the <b>Lun</b> member is valid. This value is valid only if the element type is ChangerDrive.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_NOT_BUS"></a><a id="element_status_not_bus"></a><dl>
<dt><b>ELEMENT_STATUS_NOT_BUS</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The drive at the address indicated by <b>Lun</b> and <b>TargetID</b> is on a different SCSI bus than the changer itself.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_PVOLTAG"></a><a id="element_status_pvoltag"></a><dl>
<dt><b>ELEMENT_STATUS_PVOLTAG</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Primary volume information in the <b>PrimaryVolumeID</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="ELEMENT_STATUS_SVALID"></a><a id="element_status_svalid"></a><dl>
<dt><b>ELEMENT_STATUS_SVALID</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The <b>SourceElement</b> member and ELEMENT_STATUS_INVERT are both valid.

</td>
</tr>
</table>

### -field ExceptionCode

An exception code that indicates that the element is in an abnormal state. This member is valid only if the <b>Flags</b> member includes ELEMENT_STATUS_EXCEPT. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_DRIVE_NOT_INSTALLED"></a><a id="error_drive_not_installed"></a><dl>
<dt><b>ERROR_DRIVE_NOT_INSTALLED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The drive at this element address is absent.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_LABEL_QUESTIONABLE"></a><a id="error_label_questionable"></a><dl>
<dt><b>ERROR_LABEL_QUESTIONABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The label might be invalid due to a unit attention condition.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_LABEL_UNREADABLE"></a><a id="error_label_unreadable"></a><dl>
<dt><b>ERROR_LABEL_UNREADABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The changer's barcode reader could not read the bar code label on the piece of media in this element, because the media is missing, damaged, improperly positioned, or upside down.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_SLOT_NOT_PRESENT"></a><a id="error_slot_not_present"></a><dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The slot at this element address is currently not installed in the changer. Each slot in a removable magazine is reported not present to indicate that the magazine has been removed.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_TRAY_MALFUNCTION"></a><a id="error_tray_malfunction"></a><dl>
<dt><b>ERROR_TRAY_MALFUNCTION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The drive at this element address has a tray that must be extended to load or remove media, and the tray is not extending as required.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_UNHANDLED_ERROR"></a><a id="error_unhandled_error"></a><dl>
<dt><b>ERROR_UNHANDLED_ERROR</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
Unknown error condition.

</td>
</tr>
</table>

### -field TargetId

For a SCSI changer, specifies the SCSI target ID of the drive at this element address. This member is valid only if the <b>ElementType</b> member of the <b>Element</b> structure is ChangerDrive and the <b>Flags</b> member includes ELEMENT_STATUS_ID_VALID.

### -field Lun

The SCSI logical unit number of the drive at this element address. This member is valid only if the <b>ElementType</b> member of the <b>Element</b> structure is ChangerDrive and the <b>Flags</b> member includes ELEMENT_STATUS_LUN_VALID.

### -field Reserved

Reserved for future use. The value of this member must be zero.

### -field PrimaryVolumeID

The primary volume identifier for the media. If the changer supports a barcode reader and the reader is installed (as indicated by CHANGER_BAR_CODE_SCANNER_INSTALLED in the <b>Features0</b> member of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>), <b>PrimaryVolumeID</b> is the bar code of the media. If the changer does not support a barcode reader, <b>PrimaryVolumeID</b> is the value previously assigned to the media.

This member is valid only if the <b>Flags</b> member includes ELEMENT_STATUS_PVOLTAG.

If the volume identifier is missing or unreadable, this member is cleared.

### -field AlternateVolumeID

An alternate volume identification for the media. This member is valid only for two-sided media, and pertains to the ID of the inverted side. It never represents a bar code. 




This member is valid only if the <b>Flags</b> member includes ELEMENT_STATUS_AVOLTAG.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_status_ex">CHANGER_ELEMENT_STATUS_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_get_element_status">IOCTL_CHANGER_GET_ELEMENT_STATUS</a>
