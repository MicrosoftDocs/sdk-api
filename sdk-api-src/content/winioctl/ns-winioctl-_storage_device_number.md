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

# _STORAGE_DEVICE_NUMBER structure


## -description


Contains information about a device. This structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560551">IOCTL_STORAGE_GET_DEVICE_NUMBER</a> control code.


## -struct-fields




### -field DeviceType

The type of device. Values from 0 through 32,767 are reserved for use by Microsoft. Values from 32,768 through 65,535 are reserved for use by other vendors. The following values are defined by Microsoft: 

<a id="FILE_DEVICE_8042_PORT"></a>
<a id="file_device_8042_port"></a>


#### FILE_DEVICE_8042_PORT

<a id="FILE_DEVICE_ACPI"></a>
<a id="file_device_acpi"></a>


#### FILE_DEVICE_ACPI

<a id="FILE_DEVICE_BATTERY"></a>
<a id="file_device_battery"></a>


#### FILE_DEVICE_BATTERY

<a id="FILE_DEVICE_BEEP"></a>
<a id="file_device_beep"></a>


#### FILE_DEVICE_BEEP

<a id="FILE_DEVICE_BLUETOOTH"></a>
<a id="file_device_bluetooth"></a>


#### FILE_DEVICE_BLUETOOTH

<a id="FILE_DEVICE_BUS_EXTENDER"></a>
<a id="file_device_bus_extender"></a>


#### FILE_DEVICE_BUS_EXTENDER

<a id="FILE_DEVICE_CD_ROM"></a>
<a id="file_device_cd_rom"></a>


#### FILE_DEVICE_CD_ROM

<a id="FILE_DEVICE_CD_ROM_FILE_SYSTEM"></a>
<a id="file_device_cd_rom_file_system"></a>


#### FILE_DEVICE_CD_ROM_FILE_SYSTEM

<a id="FILE_DEVICE_CHANGER"></a>
<a id="file_device_changer"></a>


#### FILE_DEVICE_CHANGER

<a id="FILE_DEVICE_CONTROLLER"></a>
<a id="file_device_controller"></a>


#### FILE_DEVICE_CONTROLLER

<a id="FILE_DEVICE_CRYPT_PROVIDER"></a>
<a id="file_device_crypt_provider"></a>


#### FILE_DEVICE_CRYPT_PROVIDER

<a id="FILE_DEVICE_DATALINK"></a>
<a id="file_device_datalink"></a>


#### FILE_DEVICE_DATALINK

<a id="FILE_DEVICE_DFS"></a>
<a id="file_device_dfs"></a>


#### FILE_DEVICE_DFS

<a id="FILE_DEVICE_DFS_FILE_SYSTEM"></a>
<a id="file_device_dfs_file_system"></a>


#### FILE_DEVICE_DFS_FILE_SYSTEM

<a id="FILE_DEVICE_DFS_VOLUME"></a>
<a id="file_device_dfs_volume"></a>


#### FILE_DEVICE_DFS_VOLUME

<a id="FILE_DEVICE_DISK"></a>
<a id="file_device_disk"></a>


#### FILE_DEVICE_DISK

<a id="FILE_DEVICE_DISK_FILE_SYSTEM"></a>
<a id="file_device_disk_file_system"></a>


#### FILE_DEVICE_DISK_FILE_SYSTEM

<a id="FILE_DEVICE_DVD"></a>
<a id="file_device_dvd"></a>


#### FILE_DEVICE_DVD

<a id="FILE_DEVICE_FILE_SYSTEM"></a>
<a id="file_device_file_system"></a>


#### FILE_DEVICE_FILE_SYSTEM

<a id="FILE_DEVICE_FIPS"></a>
<a id="file_device_fips"></a>


#### FILE_DEVICE_FIPS

<a id="FILE_DEVICE_FULLSCREEN_VIDEO"></a>
<a id="file_device_fullscreen_video"></a>


#### FILE_DEVICE_FULLSCREEN_VIDEO

<a id="FILE_DEVICE_INFINIBAND"></a>
<a id="file_device_infiniband"></a>


#### FILE_DEVICE_INFINIBAND

<a id="FILE_DEVICE_INPORT_PORT"></a>
<a id="file_device_inport_port"></a>


#### FILE_DEVICE_INPORT_PORT

<a id="FILE_DEVICE_KEYBOARD"></a>
<a id="file_device_keyboard"></a>


#### FILE_DEVICE_KEYBOARD

<a id="FILE_DEVICE_KS"></a>
<a id="file_device_ks"></a>


#### FILE_DEVICE_KS

<a id="FILE_DEVICE_KSEC"></a>
<a id="file_device_ksec"></a>


#### FILE_DEVICE_KSEC

<a id="FILE_DEVICE_MAILSLOT"></a>
<a id="file_device_mailslot"></a>


#### FILE_DEVICE_MAILSLOT

<a id="FILE_DEVICE_MASS_STORAGE"></a>
<a id="file_device_mass_storage"></a>


#### FILE_DEVICE_MASS_STORAGE

<a id="FILE_DEVICE_MIDI_IN"></a>
<a id="file_device_midi_in"></a>


#### FILE_DEVICE_MIDI_IN

<a id="FILE_DEVICE_MIDI_OUT"></a>
<a id="file_device_midi_out"></a>


#### FILE_DEVICE_MIDI_OUT

<a id="FILE_DEVICE_MODEM"></a>
<a id="file_device_modem"></a>


#### FILE_DEVICE_MODEM

<a id="FILE_DEVICE_MOUSE"></a>
<a id="file_device_mouse"></a>


#### FILE_DEVICE_MOUSE

<a id="FILE_DEVICE_MULTI_UNC_PROVIDER"></a>
<a id="file_device_multi_unc_provider"></a>


#### FILE_DEVICE_MULTI_UNC_PROVIDER

<a id="FILE_DEVICE_NAMED_PIPE"></a>
<a id="file_device_named_pipe"></a>


#### FILE_DEVICE_NAMED_PIPE

<a id="FILE_DEVICE_NETWORK"></a>
<a id="file_device_network"></a>


#### FILE_DEVICE_NETWORK

<a id="FILE_DEVICE_NETWORK_BROWSER"></a>
<a id="file_device_network_browser"></a>


#### FILE_DEVICE_NETWORK_BROWSER

<a id="FILE_DEVICE_NETWORK_FILE_SYSTEM"></a>
<a id="file_device_network_file_system"></a>


#### FILE_DEVICE_NETWORK_FILE_SYSTEM

<a id="FILE_DEVICE_NETWORK_REDIRECTOR"></a>
<a id="file_device_network_redirector"></a>


#### FILE_DEVICE_NETWORK_REDIRECTOR

<a id="FILE_DEVICE_NULL"></a>
<a id="file_device_null"></a>


#### FILE_DEVICE_NULL

<a id="FILE_DEVICE_PARALLEL_PORT"></a>
<a id="file_device_parallel_port"></a>


#### FILE_DEVICE_PARALLEL_PORT

<a id="FILE_DEVICE_PHYSICAL_NETCARD"></a>
<a id="file_device_physical_netcard"></a>


#### FILE_DEVICE_PHYSICAL_NETCARD

<a id="FILE_DEVICE_PRINTER"></a>
<a id="file_device_printer"></a>


#### FILE_DEVICE_PRINTER

<a id="FILE_DEVICE_SCANNER"></a>
<a id="file_device_scanner"></a>


#### FILE_DEVICE_SCANNER

<a id="FILE_DEVICE_SCREEN"></a>
<a id="file_device_screen"></a>


#### FILE_DEVICE_SCREEN

<a id="FILE_DEVICE_SERENUM"></a>
<a id="file_device_serenum"></a>


#### FILE_DEVICE_SERENUM

<a id="FILE_DEVICE_SERIAL_MOUSE_PORT"></a>
<a id="file_device_serial_mouse_port"></a>


#### FILE_DEVICE_SERIAL_MOUSE_PORT

<a id="FILE_DEVICE_SERIAL_PORT"></a>
<a id="file_device_serial_port"></a>


#### FILE_DEVICE_SERIAL_PORT

<a id="FILE_DEVICE_SMARTCARD"></a>
<a id="file_device_smartcard"></a>


#### FILE_DEVICE_SMARTCARD

<a id="FILE_DEVICE_SMB"></a>
<a id="file_device_smb"></a>


#### FILE_DEVICE_SMB

<a id="FILE_DEVICE_SOUND"></a>
<a id="file_device_sound"></a>


#### FILE_DEVICE_SOUND

<a id="FILE_DEVICE_STREAMS"></a>
<a id="file_device_streams"></a>


#### FILE_DEVICE_STREAMS

<a id="FILE_DEVICE_TAPE"></a>
<a id="file_device_tape"></a>


#### FILE_DEVICE_TAPE

<a id="FILE_DEVICE_TAPE_FILE_SYSTEM"></a>
<a id="file_device_tape_file_system"></a>


#### FILE_DEVICE_TAPE_FILE_SYSTEM

<a id="FILE_DEVICE_TERMSRV"></a>
<a id="file_device_termsrv"></a>


#### FILE_DEVICE_TERMSRV

<a id="FILE_DEVICE_TRANSPORT"></a>
<a id="file_device_transport"></a>


#### FILE_DEVICE_TRANSPORT

<a id="FILE_DEVICE_UNKNOWN"></a>
<a id="file_device_unknown"></a>


#### FILE_DEVICE_UNKNOWN

<a id="FILE_DEVICE_VDM"></a>
<a id="file_device_vdm"></a>


#### FILE_DEVICE_VDM

<a id="FILE_DEVICE_VIDEO"></a>
<a id="file_device_video"></a>


#### FILE_DEVICE_VIDEO

<a id="FILE_DEVICE_VIRTUAL_DISK"></a>
<a id="file_device_virtual_disk"></a>


#### FILE_DEVICE_VIRTUAL_DISK

<a id="FILE_DEVICE_VMBUS"></a>
<a id="file_device_vmbus"></a>


#### FILE_DEVICE_VMBUS

<a id="FILE_DEVICE_WAVE_IN"></a>
<a id="file_device_wave_in"></a>


#### FILE_DEVICE_WAVE_IN

<a id="FILE_DEVICE_WAVE_OUT"></a>
<a id="file_device_wave_out"></a>


#### FILE_DEVICE_WAVE_OUT

<a id="FILE_DEVICE_WPD"></a>
<a id="file_device_wpd"></a>


#### FILE_DEVICE_WPD


### -field DeviceNumber

The number of this device.


### -field PartitionNumber

The partition number of the device, if the device can be partitioned. Otherwise, this member is –1.


## -remarks



The values in the <b>STORAGE_DEVICE_NUMBER</b> structure are guaranteed to remain unchanged until the device is removed or the system is restarted. They are not guaranteed to be persistent across device or system restarts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560551">IOCTL_STORAGE_GET_DEVICE_NUMBER</a>
 

 

