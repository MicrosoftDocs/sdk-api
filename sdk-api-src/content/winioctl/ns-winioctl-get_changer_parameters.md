---
UID: NS:winioctl._GET_CHANGER_PARAMETERS
title: GET_CHANGER_PARAMETERS
description: Represents the parameters of a changer.
helpviewer_keywords: ["*PGET_CHANGER_PARAMETERS","CHANGER_BAR_CODE_SCANNER_INSTALLED","CHANGER_CARTRIDGE_MAGAZINE","CHANGER_CLEANER_ACCESS_NOT_VALID","CHANGER_CLEANER_AUTODISMOUNT","CHANGER_CLEANER_OPS_NOT_SUPPORTED","CHANGER_CLEANER_SLOT","CHANGER_CLOSE_IEPORT","CHANGER_DEVICE_REINITIALIZE_CAPABLE","CHANGER_DRIVE_CLEANING_REQUIRED","CHANGER_DRIVE_EMPTY_ON_DOOR_ACCESS","CHANGER_EXCHANGE_MEDIA","CHANGER_IEPORT_USER_CONTROL_CLOSE","CHANGER_IEPORT_USER_CONTROL_OPEN","CHANGER_INIT_ELEM_STAT_WITH_RANGE","CHANGER_KEYPAD_ENABLE_DISABLE","CHANGER_LOCK_UNLOCK","CHANGER_MEDIUM_FLIP","CHANGER_MOVE_EXTENDS_IEPORT","CHANGER_MOVE_RETRACTS_IEPORT","CHANGER_OPEN_IEPORT","CHANGER_POSITION_TO_ELEMENT","CHANGER_PREDISMOUNT_ALIGN_TO_DRIVE","CHANGER_PREDISMOUNT_ALIGN_TO_SLOT","CHANGER_PREDISMOUNT_EJECT_REQUIRED","CHANGER_PREMOUNT_EJECT_REQUIRED","CHANGER_REPORT_IEPORT_STATE","CHANGER_RTN_MEDIA_TO_ORIGINAL_ADDR","CHANGER_SERIAL_NUMBER_VALID","CHANGER_SLOTS_USE_TRAYS","CHANGER_STATUS_NON_VOLATILE","CHANGER_STORAGE_DRIVE","CHANGER_STORAGE_IEPORT","CHANGER_STORAGE_SLOT","CHANGER_STORAGE_TRANSPORT","CHANGER_TO_DRIVE","CHANGER_TO_IEPORT","CHANGER_TO_SLOT","CHANGER_TO_TRANSPORT","CHANGER_TRUE_EXCHANGE_CAPABLE","CHANGER_VOLUME_ASSERT","CHANGER_VOLUME_IDENTIFICATION","CHANGER_VOLUME_REPLACE","CHANGER_VOLUME_SEARCH","CHANGER_VOLUME_UNDEFINE","GET_CHANGER_PARAMETERS","GET_CHANGER_PARAMETERS structure","LOCK_UNLOCK_DOOR","LOCK_UNLOCK_IEPORT","LOCK_UNLOCK_KEYPAD","PGET_CHANGER_PARAMETERS","PGET_CHANGER_PARAMETERS structure pointer","_win32_get_changer_parameters_str","base.get_changer_parameters_str","winioctl/GET_CHANGER_PARAMETERS","winioctl/PGET_CHANGER_PARAMETERS"]
old-location: base\get_changer_parameters_str.htm
tech.root: base
ms.assetid: ad5b6cc3-19f1-4196-9f03-791f342d0cf9
ms.date: 12/05/2018
ms.keywords: '*PGET_CHANGER_PARAMETERS, CHANGER_BAR_CODE_SCANNER_INSTALLED, CHANGER_CARTRIDGE_MAGAZINE, CHANGER_CLEANER_ACCESS_NOT_VALID, CHANGER_CLEANER_AUTODISMOUNT, CHANGER_CLEANER_OPS_NOT_SUPPORTED, CHANGER_CLEANER_SLOT, CHANGER_CLOSE_IEPORT, CHANGER_DEVICE_REINITIALIZE_CAPABLE, CHANGER_DRIVE_CLEANING_REQUIRED, CHANGER_DRIVE_EMPTY_ON_DOOR_ACCESS, CHANGER_EXCHANGE_MEDIA, CHANGER_IEPORT_USER_CONTROL_CLOSE, CHANGER_IEPORT_USER_CONTROL_OPEN, CHANGER_INIT_ELEM_STAT_WITH_RANGE, CHANGER_KEYPAD_ENABLE_DISABLE, CHANGER_LOCK_UNLOCK, CHANGER_MEDIUM_FLIP, CHANGER_MOVE_EXTENDS_IEPORT, CHANGER_MOVE_RETRACTS_IEPORT, CHANGER_OPEN_IEPORT, CHANGER_POSITION_TO_ELEMENT, CHANGER_PREDISMOUNT_ALIGN_TO_DRIVE, CHANGER_PREDISMOUNT_ALIGN_TO_SLOT, CHANGER_PREDISMOUNT_EJECT_REQUIRED, CHANGER_PREMOUNT_EJECT_REQUIRED, CHANGER_REPORT_IEPORT_STATE, CHANGER_RTN_MEDIA_TO_ORIGINAL_ADDR, CHANGER_SERIAL_NUMBER_VALID, CHANGER_SLOTS_USE_TRAYS, CHANGER_STATUS_NON_VOLATILE, CHANGER_STORAGE_DRIVE, CHANGER_STORAGE_IEPORT, CHANGER_STORAGE_SLOT, CHANGER_STORAGE_TRANSPORT, CHANGER_TO_DRIVE, CHANGER_TO_IEPORT, CHANGER_TO_SLOT, CHANGER_TO_TRANSPORT, CHANGER_TRUE_EXCHANGE_CAPABLE, CHANGER_VOLUME_ASSERT, CHANGER_VOLUME_IDENTIFICATION, CHANGER_VOLUME_REPLACE, CHANGER_VOLUME_SEARCH, CHANGER_VOLUME_UNDEFINE, GET_CHANGER_PARAMETERS, GET_CHANGER_PARAMETERS structure, LOCK_UNLOCK_DOOR, LOCK_UNLOCK_IEPORT, LOCK_UNLOCK_KEYPAD, PGET_CHANGER_PARAMETERS, PGET_CHANGER_PARAMETERS structure pointer, _win32_get_changer_parameters_str, base.get_changer_parameters_str, winioctl/GET_CHANGER_PARAMETERS, winioctl/PGET_CHANGER_PARAMETERS'
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
req.typenames: GET_CHANGER_PARAMETERS, *PGET_CHANGER_PARAMETERS
req.redist: 
f1_keywords:
 - _GET_CHANGER_PARAMETERS
 - winioctl/_GET_CHANGER_PARAMETERS
 - PGET_CHANGER_PARAMETERS
 - winioctl/PGET_CHANGER_PARAMETERS
 - GET_CHANGER_PARAMETERS
 - winioctl/GET_CHANGER_PARAMETERS
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
 - GET_CHANGER_PARAMETERS
---

# GET_CHANGER_PARAMETERS structure


## -description

Represents the parameters of a changer.

## -struct-fields

### -field Size

The size of this structure, in bytes. The caller must set this member to <code>sizeof(GET_CHANGER_PARAMETERS)</code>.

### -field NumberTransportElements

The number of transport elements in the changer. For a SCSI changer, this is defined in the element address page. This value is almost always 1, because most changers have a single transport element with one or two picker mechanisms. A changer that has two picker mechanisms on its transport must not be represented as having two transports, because pickers are not individually addressable. High-end media libraries can have dual and multiple transport elements for fault tolerance.

### -field NumberStorageElements

The number of storage elements (slots) in the changer. For a SCSI changer, this is defined in the element address page. This value represents the maximum number of slots available for this changer including those in removable magazines, whether or not the magazines are installed. If <b>NumberCleanerSlots</b> is 1, then <b>NumberStorageElements</b> is 1 less than the maximum number of slots in the changer.

### -field NumberCleanerSlots

The number of storage elements (slots) for cleaner cartridges in the changer. If <b>NumberCleanerSlots</b> is 1, then <b>FirstCleanerSlotAddress</b> indicates the zero-based address of the slot in which a drive cleaner should be inserted. If the changer does not support drive cleaning by programmatically moving the cleaner cartridge from its slot to a drive, <b>NumberCleanerSlots</b> is 0. <b>NumberCleanerSlots</b> cannot be greater than 1.

### -field NumberIEElements

The number of import/export elements (insert/eject ports) the changer has for inserting and ejecting media. For a SCSI changer, this is defined in the element address page. An import/export element must not be part of the storage element (slot) space, and it must be possible to transport media between the import/export element and a slot using a MOVE MEDIUM command. If the changer has a door and not a true import/export element, <b>NumberIEElements</b> is 0.

### -field NumberDataTransferElements

The number of data transfer elements (drives) in the changer. For a SCSI changer, this is defined in the element address page. Unlike <b>NumberStorageElements</b>, which indicates the total number of possible slots whether or not the slots are actually present, <b>NumberDataTransferElements</b> indicates the number of drives that are actually present in the changer.

### -field NumberOfDoors

The number of doors in the changer. A door provides access to all media in the changer at once, unlike an insert/eject port, which provides access to one or more, but not all, media. A changer's door can be a physical front door or a single magazine that contains all media. If a changer supports only an insert/eject port for inserting and ejecting media, <b>NumberOfDoors</b> is 0.

### -field FirstSlotNumber

The number used by the changer vendor to identify the first storage element (slot) in the changer to the end user, either by marking a magazine or by defining a slot numbering scheme in the changer's operators guide. <b>FirstSlotNumber</b> is typically 0 or 1, but it can be the first address in a consecutive range of slot addresses defined by the vendor.

### -field FirstDriveNumber

The number used by the changer vendor to identify the first data transfer element (drive) in the changer to the end user. <b>FirstDriveNumber</b> is typically 0 or 1, but it can be the first address in a consecutive range of drive addresses defined by the vendor.

### -field FirstTransportNumber

The number used by the changer vendor to identify the first (and usually only) transport element in the changer to the end user. <b>FirstTransportNumber</b> is typically 0 or 1, but it can be the first address in a consecutive range of transport addresses defined by the vendor.

### -field FirstIEPortNumber

The number used by the changer vendor to identify the first (and usually only) insert/eject port in the changer to the end user. <b>FirstIEPortNumber</b> is typically 0 or 1, but it can be the first address in a consecutive range of insert/eject port addresses defined by the vendor. If <b>NumberIEElements</b> is 0, <b>FirstIEPortNumber</b> must also be 0.

### -field FirstCleanerSlotAddress

The number used by the changer vendor to identify the first (and only) slot address assigned to a drive cleaner cartridge to the end user. This must be the value defined by the vendor in the changer's operators guide. For example, if a changer has 8 slots numbered 1 through 8 and its operator's guide designates slot 8 as the drive cleaner slot, <b>FirstSlotNumber</b> would be 1 and <b>FirstCleanerSlotAddress</b> would be 8. If the same 8 slots were numbered 0 through 7, <b>FirstSlotNumber</b> would be 0 and <b>FirstCleanerSlotAddress</b> would be 7. If <b>NumberCleanerSlots</b> is 0, <b>FirstCleanerSlotAddress</b> must be 0.

### -field MagazineSize

The number of slots in the removable magazines in the changer. This member is valid only if CHANGER_CARTRIDGE_MAGAZINE is set in <b>Features0</b>.

### -field DriveCleanTimeout

Twice the maximum number of seconds a cleaning is expected to take. The changer's drives should be cleaned by its cleaner cartridge in half the time specified by <b>DriveCleanTimeout</b>. For example, if a drive is typically cleaned in 300 seconds (5 minutes), <b>DriveCleanTimeout</b> should be set to 600.

### -field Features0

The features supported by the changer. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHANGER_BAR_CODE_SCANNER_INSTALLED"></a><a id="changer_bar_code_scanner_installed"></a><dl>
<dt><b>CHANGER_BAR_CODE_SCANNER_INSTALLED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The changer supports a bar-code reader and the reader is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CARTRIDGE_MAGAZINE"></a><a id="changer_cartridge_magazine"></a><dl>
<dt><b>CHANGER_CARTRIDGE_MAGAZINE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The changer uses removable cartridge magazines for some or all storage slots.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CLEANER_ACCESS_NOT_VALID"></a><a id="changer_cleaner_access_not_valid"></a><dl>
<dt><b>CHANGER_CLEANER_ACCESS_NOT_VALID</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The ELEMENT_STATUS_ACCESS flag in a 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_status">CHANGER_ELEMENT_STATUS</a> structure for a data transport element is invalid when the transport element contains a cleaning cartridge.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CLEANER_SLOT"></a><a id="changer_cleaner_slot"></a><dl>
<dt><b>CHANGER_CLEANER_SLOT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The changer has a slot designated for a cleaner cartridge. If this flag is set, <b>NumberCleanerSlots</b> must be 1 and <b>FirstCleanerSlotAddress</b> must specify the address of the cleaner slot.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CLOSE_IEPORT"></a><a id="changer_close_ieport"></a><dl>
<dt><b>CHANGER_CLOSE_IEPORT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The changer has an insert/eject port and can retract the insert/eject port programmatically.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_DEVICE_REINITIALIZE_CAPABLE"></a><a id="changer_device_reinitialize_capable"></a><dl>
<dt><b>CHANGER_DEVICE_REINITIALIZE_CAPABLE</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
The changer can recalibrate its transport element in response to an explicit command.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_DRIVE_CLEANING_REQUIRED"></a><a id="changer_drive_cleaning_required"></a><dl>
<dt><b>CHANGER_DRIVE_CLEANING_REQUIRED</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The changer's drives require periodic cleaning, which must be initiated by either the user or an application, and the changer can use its transport element to mount a cleaner cartridge in a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_DRIVE_EMPTY_ON_DOOR_ACCESS"></a><a id="changer_drive_empty_on_door_access"></a><dl>
<dt><b>CHANGER_DRIVE_EMPTY_ON_DOOR_ACCESS</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The changer requires all drives to be empty (dismounted) before they can be accessed through its door.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_EXCHANGE_MEDIA"></a><a id="changer_exchange_media"></a><dl>
<dt><b>CHANGER_EXCHANGE_MEDIA</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The changer can exchange media between elements. For a SCSI changer, this flag indicates whether the changer supports the EXCHANGE MEDIUM command.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_INIT_ELEM_STAT_WITH_RANGE"></a><a id="changer_init_elem_stat_with_range"></a><dl>
<dt><b>CHANGER_INIT_ELEM_STAT_WITH_RANGE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The changer can initialize elements within a specified range. For a SCSI changer, this flag indicates whether the changer supports the INITIALIZE ELEMENT STATUS WITH RANGE command.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_KEYPAD_ENABLE_DISABLE"></a><a id="changer_keypad_enable_disable"></a><dl>
<dt><b>CHANGER_KEYPAD_ENABLE_DISABLE</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The changer keypad can be enabled and disabled programmatically.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_LOCK_UNLOCK"></a><a id="changer_lock_unlock"></a><dl>
<dt><b>CHANGER_LOCK_UNLOCK</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The changer's door, insert/eject port, or keypad can be locked or unlocked programmatically. If this flag is set, <b>LockUnlockCapabilities</b> indicates which elements can be locked or unlocked.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_MEDIUM_FLIP"></a><a id="changer_medium_flip"></a><dl>
<dt><b>CHANGER_MEDIUM_FLIP</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The changer's transport element supports flipping (rotating) media. For a SCSI changer, this flag reflects the rotate bit in the transport geometry parameters page.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_OPEN_IEPORT"></a><a id="changer_open_ieport"></a><dl>
<dt><b>CHANGER_OPEN_IEPORT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The changer has an insert/eject port and can extend the insert/eject port programmatically.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_POSITION_TO_ELEMENT"></a><a id="changer_position_to_element"></a><dl>
<dt><b>CHANGER_POSITION_TO_ELEMENT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The changer can position the transport to a particular destination. For a SCSI changer, this flag indicates whether the changer supports the POSITION TO ELEMENT command. If this flag is set, <b>PositionCapabilities</b> indicates the elements to which the transport can be positioned.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_PREDISMOUNT_EJECT_REQUIRED"></a><a id="changer_predismount_eject_required"></a><dl>
<dt><b>CHANGER_PREDISMOUNT_EJECT_REQUIRED</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The changer requires an explicit command issued through a mass-storage driver (tape, disk, or CDROM, for example) to eject media from a drive before the changer can move the media from a drive to a slot.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_PREMOUNT_EJECT_REQUIRED"></a><a id="changer_premount_eject_required"></a><dl>
<dt><b>CHANGER_PREMOUNT_EJECT_REQUIRED</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The changer requires an explicit command issued through a mass storage driver to eject a drive mechanism before the changer can move media from a slot to the drive. For example, a changer with CD-ROM drives might require the tray to be presented to the robotic transport so that a piece of media could be loaded onto the tray during a mount operation.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_REPORT_IEPORT_STATE"></a><a id="changer_report_ieport_state"></a><dl>
<dt><b>CHANGER_REPORT_IEPORT_STATE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The changer can report whether media is present in the insert/eject port. Such a changer must have a sensor in the insert/eject port to detect the presence or absence of media.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_SERIAL_NUMBER_VALID"></a><a id="changer_serial_number_valid"></a><dl>
<dt><b>CHANGER_SERIAL_NUMBER_VALID</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The serial number is valid and unique for all changers of this type. Serial numbers are not guaranteed to be unique across vendor and product lines.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_STATUS_NON_VOLATILE"></a><a id="changer_status_non_volatile"></a><dl>
<dt><b>CHANGER_STATUS_NON_VOLATILE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The changer uses nonvolatile memory for element status information.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_STORAGE_DRIVE"></a><a id="changer_storage_drive"></a><dl>
<dt><b>CHANGER_STORAGE_DRIVE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The changer can use a drive as an independent storage element; that is, it can store media in the drive without reading it. For a SCSI changer, this flag reflects the state of the DT bit in the device capabilities page.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_STORAGE_IEPORT"></a><a id="changer_storage_ieport"></a><dl>
<dt><b>CHANGER_STORAGE_IEPORT</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The changer can use an insert/eject port as an independent storage element. For a SCSI changer, this flag reflects the state of the I/E bit in the device capabilities page.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_STORAGE_SLOT"></a><a id="changer_storage_slot"></a><dl>
<dt><b>CHANGER_STORAGE_SLOT</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
The changer can use a slot as an independent storage element for media. For a SCSI changer, this flag reflects the state of the ST bit in the device capabilities page. Slots are the normal storage location for media, so the changer must support this functionality.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_STORAGE_TRANSPORT"></a><a id="changer_storage_transport"></a><dl>
<dt><b>CHANGER_STORAGE_TRANSPORT</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The changer can use a transport as an independent storage element. For a SCSI changer, this flag reflects the state of the MT bit in the device capabilities page.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_VOLUME_ASSERT"></a><a id="changer_volume_assert"></a><dl>
<dt><b>CHANGER_VOLUME_ASSERT</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
The changer can verify volume information. For a SCSI changer, this flag indicates whether the changer supports the SEND VOLUME TAG command with a send action code of ASSERT.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_VOLUME_IDENTIFICATION"></a><a id="changer_volume_identification"></a><dl>
<dt><b>CHANGER_VOLUME_IDENTIFICATION</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The changer supports volume identification. For a SCSI changer, this flag indicates whether the changer supports the SEND VOLUME TAG and REQUEST VOLUME ELEMENT ADDRESS commands.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_VOLUME_REPLACE"></a><a id="changer_volume_replace"></a><dl>
<dt><b>CHANGER_VOLUME_REPLACE</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The changer can replace volume information. For a SCSI changer, this flag indicates whether the changer supports the SEND VOLUME TAG command with a send action code of REPLACE.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_VOLUME_SEARCH"></a><a id="changer_volume_search"></a><dl>
<dt><b>CHANGER_VOLUME_SEARCH</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
The changer can search for volume information. For a SCSI changer, this flag indicates whether the changer supports the supports the SEND VOLUME TAG command with a send action code of TRANSLATE.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_VOLUME_UNDEFINE"></a><a id="changer_volume_undefine"></a><dl>
<dt><b>CHANGER_VOLUME_UNDEFINE</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The changer can clear existing volume information. For a SCSI changer, this flag indicates whether the changer supports the SEND VOLUME TAG command with a send action code of UNDEFINE.

</td>
</tr>
</table>

### -field Features1

Any additional features supported by the changer. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CLEANER_AUTODISMOUNT"></a><a id="changer_cleaner_autodismount"></a><dl>
<dt><b>CHANGER_CLEANER_AUTODISMOUNT</b></dt>
<dt>0x80000004</dt>
</dl>
</td>
<td width="60%">
The changer will move the cleaning cartridge back to its original slot automatically after cleaning is finished.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_CLEANER_OPS_NOT_SUPPORTED"></a><a id="changer_cleaner_ops_not_supported"></a><dl>
<dt><b>CHANGER_CLEANER_OPS_NOT_SUPPORTED</b></dt>
<dt>0x80000040</dt>
</dl>
</td>
<td width="60%">
The changer does not support automatic cleaning of its elements.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_IEPORT_USER_CONTROL_CLOSE"></a><a id="changer_ieport_user_control_close"></a><dl>
<dt><b>CHANGER_IEPORT_USER_CONTROL_CLOSE</b></dt>
<dt>0x80000100</dt>
</dl>
</td>
<td width="60%">
The changer requires the user to manually close an open insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_IEPORT_USER_CONTROL_OPEN"></a><a id="changer_ieport_user_control_open"></a><dl>
<dt><b>CHANGER_IEPORT_USER_CONTROL_OPEN</b></dt>
<dt>0x80000080</dt>
</dl>
</td>
<td width="60%">
The changer requires the user to manually open a closed insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_MOVE_EXTENDS_IEPORT"></a><a id="changer_move_extends_ieport"></a><dl>
<dt><b>CHANGER_MOVE_EXTENDS_IEPORT</b></dt>
<dt>0x80000200</dt>
</dl>
</td>
<td width="60%">
The changer will extend the tray automatically whenever a command is issued to move media to an insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_MOVE_RETRACTS_IEPORT"></a><a id="changer_move_retracts_ieport"></a><dl>
<dt><b>CHANGER_MOVE_RETRACTS_IEPORT</b></dt>
<dt>0x80000400</dt>
</dl>
</td>
<td width="60%">
The changer will retract the tray automatically whenever a command is issued to move media from an insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_PREDISMOUNT_ALIGN_TO_DRIVE"></a><a id="changer_predismount_align_to_drive"></a><dl>
<dt><b>CHANGER_PREDISMOUNT_ALIGN_TO_DRIVE</b></dt>
<dt>0x80000002</dt>
</dl>
</td>
<td width="60%">
The changer requires an explicit command to position the transport element to a drive before it can eject media from the drive.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_PREDISMOUNT_ALIGN_TO_SLOT"></a><a id="changer_predismount_align_to_slot"></a><dl>
<dt><b>CHANGER_PREDISMOUNT_ALIGN_TO_SLOT</b></dt>
<dt>0x80000001</dt>
</dl>
</td>
<td width="60%">
The changer requires an explicit command to position the transport element to a slot before it can eject media from the slot.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_RTN_MEDIA_TO_ORIGINAL_ADDR"></a><a id="changer_rtn_media_to_original_addr"></a><dl>
<dt><b>CHANGER_RTN_MEDIA_TO_ORIGINAL_ADDR</b></dt>
<dt>0x80000020</dt>
</dl>
</td>
<td width="60%">
The changer requires media to be returned to its original slot after it has been moved.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_SLOTS_USE_TRAYS"></a><a id="changer_slots_use_trays"></a><dl>
<dt><b>CHANGER_SLOTS_USE_TRAYS</b></dt>
<dt>0x80000010</dt>
</dl>
</td>
<td width="60%">
The changer uses removable trays in its slots, which require the media to be placed in a tray and the tray moved to the desired position.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_TRUE_EXCHANGE_CAPABLE"></a><a id="changer_true_exchange_capable"></a><dl>
<dt><b>CHANGER_TRUE_EXCHANGE_CAPABLE</b></dt>
<dt>0x80000008</dt>
</dl>
</td>
<td width="60%">
The changer can exchange media between a source and a destination in a single operation. This flag is valid only if CHANGER_EXCHANGE_MEDIA is also set in <b>Features0</b>.

</td>
</tr>
</table>

### -field MoveFromTransport

Indicates whether the changer supports moving a piece of media from a transport element to another transport element, a storage slot, an insert/eject port, or a drive. For a SCSI changer, this is defined in the device capabilities page. The transport is not typically the source or destination for moving or exchanging media. 




To determine whether the changer can move media to a given element, use the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHANGER_TO_DRIVE"></a><a id="changer_to_drive"></a><dl>
<dt><b>CHANGER_TO_DRIVE</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The changer can carry out the operation from the specified element to a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_TO_IEPORT"></a><a id="changer_to_ieport"></a><dl>
<dt><b>CHANGER_TO_IEPORT</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The changer can carry out the operation from the specified element to an insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_TO_SLOT"></a><a id="changer_to_slot"></a><dl>
<dt><b>CHANGER_TO_SLOT</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The changer can carry out the operation from the specified element to a storage slot.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGER_TO_TRANSPORT"></a><a id="changer_to_transport"></a><dl>
<dt><b>CHANGER_TO_TRANSPORT</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The changer can carry out the operation from the specified element to a transport.

</td>
</tr>
</table>

### -field MoveFromSlot

Indicates whether the changer supports moving medium from a storage slot to a transport element, another storage slot, an insert/eject port, or a drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the move.

### -field MoveFromIePort

Indicates whether the changer supports moving medium from an insert/eject port to a transport element, a storage slot, another insert/eject port, or a drive. For a SCSI changer, this is defined in the device capabilities page. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the move.

### -field MoveFromDrive

Indicates whether the changer supports moving medium from a drive to a transport element, a storage slot, an insert/eject port, or another drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the move.

### -field ExchangeFromTransport

Indicates whether the changer supports exchanging medium between a transport element and another transport element, a storage slot, an insert/eject port, or a drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the exchange.

### -field ExchangeFromSlot

Indicates whether the changer supports exchanging medium between a storage slot and a transport element, another storage slot, an insert/eject port, or a drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the exchange.

### -field ExchangeFromIePort

Indicates whether the changer supports exchanging medium between an insert/eject port and a transport element, a storage slot, another insert/eject port, or a drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the exchange.

### -field ExchangeFromDrive

Indicates whether the changer supports exchanging medium between a drive and a transport element, a storage slot, an insert/eject port, or another drive. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports the exchange.

### -field LockUnlockCapabilities

The elements of a changer that can be locked or unlocked programmatically. This member is valid only if CHANGER_LOCK_UNLOCK is set in <b>Features0</b>. 




To determine whether the changer can lock or unlock a particular element, use one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOCK_UNLOCK_DOOR"></a><a id="lock_unlock_door"></a><dl>
<dt><b>LOCK_UNLOCK_DOOR</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The changer can lock or unlock its door.

</td>
</tr>
<tr>
<td width="40%"><a id="LOCK_UNLOCK_IEPORT"></a><a id="lock_unlock_ieport"></a><dl>
<dt><b>LOCK_UNLOCK_IEPORT</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The changer can lock or unlock its insert/eject port.

</td>
</tr>
<tr>
<td width="40%"><a id="LOCK_UNLOCK_KEYPAD"></a><a id="lock_unlock_keypad"></a><dl>
<dt><b>LOCK_UNLOCK_KEYPAD</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The changer can lock or unlock its keypad.

</td>
</tr>
</table>

### -field PositionCapabilities

The elements to which a changer can position its transport. Use the flags described under <b>MoveFromTransport</b> to determine whether the changer supports positioning the transport to a particular element. This member is valid only if CHANGER_POSITION_TO_ELEMENT is set in <b>Features0</b>.

### -field Reserved1

Reserved for future use.

### -field Reserved2

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_get_parameters">IOCTL_CHANGER_GET_PARAMETERS</a>