---
UID: NS:iscsidsc.ISCSI_DEVICE_ON_SESSIONW
title: ISCSI_DEVICE_ON_SESSIONW (iscsidsc.h)
description: ISCSI_DEVICE_ON_SESSION structure specifies multiple methods for identifying a device associated with an iSCSI login session. (Unicode)
helpviewer_keywords: ["*PISCSI_DEVICE_ON_SESSIONW","ISCSI_DEVICE_ON_SESSION","ISCSI_DEVICE_ON_SESSION structure [iSCSI Discovery Library API]","ISCSI_DEVICE_ON_SESSIONA","ISCSI_DEVICE_ON_SESSIONW","PISCSI_DEVICE_ON_SESSION","PISCSI_DEVICE_ON_SESSION structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_device_on_session","iscsidsc/ISCSI_DEVICE_ON_SESSION","iscsidsc/ISCSI_DEVICE_ON_SESSIONA","iscsidsc/ISCSI_DEVICE_ON_SESSIONW","iscsidsc/PISCSI_DEVICE_ON_SESSION"]
old-location: iscsidisc\iscsi_device_on_session.htm
tech.root: iSCSIDisc
ms.assetid: ea5d01ee-64c7-43bb-8945-af38d06de36c
ms.date: 12/05/2018
ms.keywords: '*PISCSI_DEVICE_ON_SESSIONW, ISCSI_DEVICE_ON_SESSION, ISCSI_DEVICE_ON_SESSION structure [iSCSI Discovery Library API], ISCSI_DEVICE_ON_SESSIONA, ISCSI_DEVICE_ON_SESSIONW, PISCSI_DEVICE_ON_SESSION, PISCSI_DEVICE_ON_SESSION structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_device_on_session, iscsidsc/ISCSI_DEVICE_ON_SESSION, iscsidsc/ISCSI_DEVICE_ON_SESSIONA, iscsidsc/ISCSI_DEVICE_ON_SESSIONW, iscsidsc/PISCSI_DEVICE_ON_SESSION'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_DEVICE_ON_SESSIONW (Unicode) and ISCSI_DEVICE_ON_SESSIONA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISCSI_DEVICE_ON_SESSIONW, *PISCSI_DEVICE_ON_SESSIONW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_DEVICE_ON_SESSIONW
 - iscsidsc/PISCSI_DEVICE_ON_SESSIONW
 - ISCSI_DEVICE_ON_SESSIONW
 - iscsidsc/ISCSI_DEVICE_ON_SESSIONW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_DEVICE_ON_SESSION
 - ISCSI_DEVICE_ON_SESSIONA
 - ISCSI_DEVICE_ON_SESSIONW
---

# ISCSI_DEVICE_ON_SESSIONW structure


## -description

The <b>ISCSI_DEVICE_ON_SESSION</b> structure specifies multiple methods for identifying a device associated with an iSCSI login session.

## -struct-fields

### -field InitiatorName

A string that indicates the initiator name.

### -field TargetName

A string that indicates the target name.

### -field ScsiAddress

A SCSI_ADDRESS structure that contains the SCSI address of the device.

### -field DeviceInterfaceType

A GUID that specifies the device interface class associated with the device. Device interface class GUIDs include, but are not limited to, the following:

<table>
<tr>
<th>GUID</th>
<th>Type of Device</th>
</tr>
<tr>
<td>GUID_DEVINTERFACE_DISK</td>
<td>Disk</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_TAPE</td>
<td>Tape</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_CDROM</td>
<td>CD-ROM</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_WRITEONCEDISK</td>
<td>Write Once Disk</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_CDCHANGER</td>
<td>CD Changer</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_MEDIUMCHANGER</td>
<td>Medium Changer</td>
</tr>
<tr>
<td>GUID_DEVINTERFACE_FLOPPY</td>
<td>Floppy</td>
</tr>
</table>

### -field DeviceInterfaceName

A string that specifies the name of the device interface class.

### -field LegacyName

A string that specifies the legacy device name.

### -field StorageDeviceNumber

A <b>STORAGE_DEVICE_NUMBER</b> structure containing the storage device number.

### -field DeviceInstance

A handle to the instance of the device in the devnode tree. For information on the cfgmgr32Xxx functions that utilize this handle, see PnP Configuration Manager Functions.

## -see-also

<b>SCSI_ADDRESS</b>



<b>STORAGE_DEVICE_NUMBER</b>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ISCSI_DEVICE_ON_SESSION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

