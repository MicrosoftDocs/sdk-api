---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISCSI_DEVICE_ON_SESSIONA structure


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
 

 

