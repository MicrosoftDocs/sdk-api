---
UID: NS:ntmsapi._NTMS_CHANGERTYPEINFORMATIONA
title: NTMS_CHANGERTYPEINFORMATIONA (ntmsapi.h)
description: The NTMS_CHANGERTYPEINFORMATION structure defines the properties specific to a type of robotic changer supported by RSM. (ANSI)
helpviewer_keywords: ["FILE_DEVICE_CHANGER","NTMS_CHANGERTYPEINFORMATION","NTMS_CHANGERTYPEINFORMATION structure [Files]","NTMS_CHANGERTYPEINFORMATIONA","NTMS_CHANGERTYPEINFORMATIONW","_NTMS_CHANGERTYPEINFORMATIONA","_NTMS_CHANGERTYPEINFORMATIONW","_zaw_ntms_changertypeinformation","base.ntms_changertypeinformation","fs.ntms_changertypeinformation","ntmsapi/NTMS_CHANGERTYPEINFORMATION"]
old-location: fs\ntms_changertypeinformation.htm
tech.root: fs
ms.assetid: 49c219d7-5772-4868-80dd-ab1e1f1471b1
ms.date: 12/05/2018
ms.keywords: FILE_DEVICE_CHANGER, NTMS_CHANGERTYPEINFORMATION, NTMS_CHANGERTYPEINFORMATION structure [Files], NTMS_CHANGERTYPEINFORMATIONA, NTMS_CHANGERTYPEINFORMATIONW, _NTMS_CHANGERTYPEINFORMATIONA, _NTMS_CHANGERTYPEINFORMATIONW, _zaw_ntms_changertypeinformation, base.ntms_changertypeinformation, fs.ntms_changertypeinformation, ntmsapi/NTMS_CHANGERTYPEINFORMATION
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
req.typenames: NTMS_CHANGERTYPEINFORMATIONA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_CHANGERTYPEINFORMATIONA
 - ntmsapi/_NTMS_CHANGERTYPEINFORMATIONA
 - NTMS_CHANGERTYPEINFORMATIONA
 - ntmsapi/NTMS_CHANGERTYPEINFORMATIONA
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
 - NTMS_CHANGERTYPEINFORMATION
 - NTMS_CHANGERTYPEINFORMATIONA
 - NTMS_CHANGERTYPEINFORMATIONW
---

# NTMS_CHANGERTYPEINFORMATIONA structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_CHANGERTYPEINFORMATION</b> structure defines the properties specific to a type of robotic changer supported by RSM.

## -struct-fields

### -field szVendor

Name of the vendor of the changer. This is acquired directly from the device inquiry data.

### -field szProduct

Product name of the changer. This is acquired directly from the device inquiry data.

### -field DeviceType

SCSI device type as reported from device inquiry data. From Winioctl.h. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_DEVICE_CHANGER"></a><a id="file_device_changer"></a><dl>
<dt><b>FILE_DEVICE_CHANGER</b></dt>
</dl>
</td>
<td width="60%">
Changer device.

</td>
</tr>
</table>

## -remarks

The 
<b>NTMS_CHANGERTYPEINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_CHANGERTYPEINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
