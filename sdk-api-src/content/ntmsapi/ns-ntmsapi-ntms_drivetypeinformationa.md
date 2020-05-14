---
UID: NS:ntmsapi._NTMS_DRIVETYPEINFORMATIONA
title: NTMS_DRIVETYPEINFORMATIONA (ntmsapi.h)
description: The NTMS_DRIVETYPEINFORMATION structure defines the properties specific to a type of drive supported by RSM.helpviewer_keywords: ["FILE_DEVICE_CD_ROM","FILE_DEVICE_DISK","FILE_DEVICE_DVD","FILE_DEVICE_TAPE","NTMS_DRIVETYPEINFORMATION","NTMS_DRIVETYPEINFORMATION structure [Files]","NTMS_DRIVETYPEINFORMATIONA","NTMS_DRIVETYPEINFORMATIONW","_NTMS_DRIVETYPEINFORMATIONA","_NTMS_DRIVETYPEINFORMATIONW","_zaw_ntms_drivetypeinformation","base.ntms_drivetypeinformation","fs.ntms_drivetypeinformation","ntmsapi/NTMS_DRIVETYPEINFORMATION"]
old-location: fs\ntms_drivetypeinformation.htm
tech.root: Rsm
ms.assetid: 2c852397-540c-44f9-a94e-2100d1588d75
ms.date: 12/05/2018
ms.keywords: FILE_DEVICE_CD_ROM, FILE_DEVICE_DISK, FILE_DEVICE_DVD, FILE_DEVICE_TAPE, NTMS_DRIVETYPEINFORMATION, NTMS_DRIVETYPEINFORMATION structure [Files], NTMS_DRIVETYPEINFORMATIONA, NTMS_DRIVETYPEINFORMATIONW, _NTMS_DRIVETYPEINFORMATIONA, _NTMS_DRIVETYPEINFORMATIONW, _zaw_ntms_drivetypeinformation, base.ntms_drivetypeinformation, fs.ntms_drivetypeinformation, ntmsapi/NTMS_DRIVETYPEINFORMATION
f1_keywords:
- ntmsapi/NTMS_DRIVETYPEINFORMATION
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntmsapi.h
api_name:
- NTMS_DRIVETYPEINFORMATION
- NTMS_DRIVETYPEINFORMATIONA
- NTMS_DRIVETYPEINFORMATIONW
targetos: Windows
req.typenames: NTMS_DRIVETYPEINFORMATIONA
req.redist: 
ms.custom: 19H1
---

# NTMS_DRIVETYPEINFORMATIONA structure


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_DRIVETYPEINFORMATION</b> structure defines the properties specific to a type of drive supported by RSM.


## -struct-fields




### -field szVendor

Name of the vendor of the drive. This is acquired directly from the device inquiry data.


### -field szProduct

Name of the product of the drive. This is acquired directly from the device inquiry data.


### -field NumberOfHeads

This member is reserved for future use and should be ignored.


### -field DeviceType

The SCSI device type as reported from device inquiry data. From Winioctl.h. This can be one of the following values. 



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
<td width="40%"><a id="FILE_DEVICE_DVD"></a><a id="file_device_dvd"></a><dl>
<dt><b>FILE_DEVICE_DVD</b></dt>
</dl>
</td>
<td width="60%">
DVD device

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
<b>NTMS_DRIVETYPEINFORMATION</b> structure is included in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
 

 

