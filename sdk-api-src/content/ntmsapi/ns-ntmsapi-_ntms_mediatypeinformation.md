---
UID: NS:ntmsapi._NTMS_MEDIATYPEINFORMATION
title: "_NTMS_MEDIATYPEINFORMATION"
author: windows-driver-content
description: The NTMS_MEDIATYPEINFORMATION structure defines the properties specific to a type of media supported by RSM.
old-location: fs\ntms_mediatypeinformation.htm
old-project: Rsm
ms.assetid: 38020a77-0340-4096-a2a8-d16eec5857e6
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: FILE_DEVICE_CD_ROM, FILE_DEVICE_DISK, FILE_DEVICE_TAPE, NTMS_MEDIARW_READONLY, NTMS_MEDIARW_REWRITABLE, NTMS_MEDIARW_WRITEONCE, NTMS_MEDIATYPEINFORMATION, NTMS_MEDIATYPEINFORMATION structure [Files], _NTMS_MEDIATYPEINFORMATION, _zaw_ntms_mediatypeinformation, base.ntms_mediatypeinformation, fs.ntms_mediatypeinformation, ntmsapi/NTMS_MEDIATYPEINFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NTMS_MEDIATYPEINFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntmsapi.h
api_name:
-	NTMS_MEDIATYPEINFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NTMS_MEDIATYPEINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_MEDIATYPEINFORMATION</b> structure defines the properties specific to a type of media supported by RSM.


## -struct-fields




### -field MediaType

Each disk or tape driver reports the media-type enumeration value of the medium that is currently mounted in the drive. This member can be one of the values in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566992">STORAGE_MEDIA_TYPE</a> enumeration type. This unique media type value is mapped to a human-readable string in the object <b>szName</b> member.


### -field NumberOfSides

Number of sides on the media.


### -field ReadWriteCharacteristics

Identifies the read/write characteristics of the media type. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIARW_REWRITABLE"></a><a id="ntms_mediarw_rewritable"></a><dl>
<dt><b>NTMS_MEDIARW_REWRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Media that can be rewritten. This includes magnetic tape, magnetic disk, and some optical disk media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIARW_WRITEONCE"></a><a id="ntms_mediarw_writeonce"></a><dl>
<dt><b>NTMS_MEDIARW_WRITEONCE</b></dt>
</dl>
</td>
<td width="60%">
Media that can only be written to one time. Some optical media, for example, 5.25", 12", 14" WORM, and CD-R, are designed to be write-once.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MEDIARW_READONLY"></a><a id="ntms_mediarw_readonly"></a><dl>
<dt><b>NTMS_MEDIARW_READONLY</b></dt>
</dl>
</td>
<td width="60%">
Media that cannot be written to CD-ROM and DVD-ROM.

</td>
</tr>
</table>
 


### -field DeviceType

SCSI device type as reported from device inquiry data. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_DEVICE_CD_ROM"></a><a id="file_device_cd_rom"></a><dl>
<dt><b>FILE_DEVICE_CD_ROM</b></dt>
</dl>
</td>
<td width="60%">
CD-ROM device.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_DEVICE_DISK"></a><a id="file_device_disk"></a><dl>
<dt><b>FILE_DEVICE_DISK</b></dt>
</dl>
</td>
<td width="60%">
Direct access device.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_DEVICE_TAPE"></a><a id="file_device_tape"></a><dl>
<dt><b>FILE_DEVICE_TAPE</b></dt>
</dl>
</td>
<td width="60%">
Sequential access device.

</td>
</tr>
</table>
 


## -remarks



The 
<b>NTMS_MEDIATYPEINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

