---
UID: NE:winnt._FIRMWARE_TYPE
title: "_FIRMWARE_TYPE"
author: windows-sdk-content
description: Specifies a firmware type.
old-location: base\firmware_type.htm
tech.root: SysInfo
ms.assetid: c058e20e-11f9-4652-b658-9fd0a43d4224
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PFIRMWARE_TYPE, FIRMWARE_TYPE, FIRMWARE_TYPE enumeration, FirmwareTypeBios, FirmwareTypeMax, FirmwareTypeUefi, FirmwareTypeUnknown, PFIRMWARE_TYPE, PFIRMWARE_TYPE enumeration pointer, _FIRMWARE_TYPE, base.firmware_type, winnt/FIRMWARE_TYPE, winnt/FirmwareTypeBios, winnt/FirmwareTypeMax, winnt/FirmwareTypeUefi, winnt/FirmwareTypeUnknown, winnt/PFIRMWARE_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: FIRMWARE_TYPE, *PFIRMWARE_TYPE
req.redist: 
---

# _FIRMWARE_TYPE enumeration


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




<a href="https://msdn.microsoft.com/db1f6889-067a-4a5d-bbfa-5836287d08ca">GetFirmwareType</a>
 

 

