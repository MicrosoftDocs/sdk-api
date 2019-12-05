---
UID: NE:winnt._FIRMWARE_TYPE
title: FIRMWARE_TYPE (winnt.h)
description: Specifies a firmware type.
old-location: base\firmware_type.htm
tech.root: SysInfo
ms.assetid: c058e20e-11f9-4652-b658-9fd0a43d4224
ms.date: 12/05/2018
ms.keywords: '*PFIRMWARE_TYPE, FIRMWARE_TYPE, FIRMWARE_TYPE enumeration, FirmwareTypeBios, FirmwareTypeMax, FirmwareTypeUefi, FirmwareTypeUnknown, PFIRMWARE_TYPE, PFIRMWARE_TYPE enumeration pointer, base.firmware_type, winnt/FIRMWARE_TYPE, winnt/FirmwareTypeBios, winnt/FirmwareTypeMax, winnt/FirmwareTypeUefi, winnt/FirmwareTypeUnknown, winnt/PFIRMWARE_TYPE'
ms.topic: enum
f1_keywords:
- winnt/FIRMWARE_TYPE
dev_langs:
- c++
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- Winnt.h
api_name:
- FIRMWARE_TYPE
targetos: Windows
req.typenames: FIRMWARE_TYPE, *PFIRMWARE_TYPE
req.redist: 
ms.custom: 19H1
---

# FIRMWARE_TYPE enumeration


## -description


Specifies a firmware type.


## -enum-fields




### -field FirmwareTypeUnknown

The firmware type is unknown.


### -field FirmwareTypeBios

The computer booted in legacy BIOS mode.


### -field FirmwareTypeUefi

The computer booted in UEFI mode.


### -field FirmwareTypeMax

Not implemented.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfirmwaretype">GetFirmwareType</a>
 

 

