---
UID: NS:ntmsapi._NTMS_CHANGERINFORMATIONW
title: NTMS_CHANGERINFORMATIONW (ntmsapi.h)
description: The NTMS_CHANGERINFORMATION structure defines properties specific to a robotic changer object. (Unicode)
helpviewer_keywords: ["NTMS_CHANGERINFORMATION","NTMS_CHANGERINFORMATION structure [Files]","NTMS_CHANGERINFORMATIONA","NTMS_CHANGERINFORMATIONW","_NTMS_CHANGERINFORMATIONA","_NTMS_CHANGERINFORMATIONW","_zaw_ntms_changerinformation","base.ntms_changerinformation","fs.ntms_changerinformation","ntmsapi/NTMS_CHANGERINFORMATION"]
old-location: fs\ntms_changerinformation.htm
tech.root: fs
ms.assetid: 2aa9fccf-dea3-4fa3-9fbf-6d83770c3893
ms.date: 12/05/2018
ms.keywords: NTMS_CHANGERINFORMATION, NTMS_CHANGERINFORMATION structure [Files], NTMS_CHANGERINFORMATIONA, NTMS_CHANGERINFORMATIONW, _NTMS_CHANGERINFORMATIONA, _NTMS_CHANGERINFORMATIONW, _zaw_ntms_changerinformation, base.ntms_changerinformation, fs.ntms_changerinformation, ntmsapi/NTMS_CHANGERINFORMATION
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
req.typenames: NTMS_CHANGERINFORMATIONW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_CHANGERINFORMATIONW
 - ntmsapi/_NTMS_CHANGERINFORMATIONW
 - NTMS_CHANGERINFORMATIONW
 - ntmsapi/NTMS_CHANGERINFORMATIONW
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
 - NTMS_CHANGERINFORMATION
 - NTMS_CHANGERINFORMATIONA
 - NTMS_CHANGERINFORMATIONW
---

# NTMS_CHANGERINFORMATIONW structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_CHANGERINFORMATION</b> structure defines properties specific to a robotic changer object.

## -struct-fields

### -field Number

Number of the changer within the library.

### -field ChangerType

Identifier of the changer type of this changer.

### -field szSerialNumber

Serial number for the changer represented as a string. Devices that do not support serial numbers report <b>NULL</b> for this member.

### -field szRevision

Revision for the changer, represented as a string.

### -field szDeviceName

Name of the device used to access the changer.

### -field ScsiPort

SCSI host adapter to which the changer is connected.

### -field ScsiBus

SCSI bus to which the changer is connected.

### -field ScsiTarget

SCSI target ID for the changer.

### -field ScsiLun

SCSI logical unit ID for the changer.

### -field Library

Unique identifier of the library that contains the changer.

## -remarks

The 
<b>NTMS_CHANGERINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_CHANGERINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
