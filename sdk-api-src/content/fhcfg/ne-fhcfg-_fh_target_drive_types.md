---
UID: NE:fhcfg._FH_TARGET_DRIVE_TYPES
title: "_FH_TARGET_DRIVE_TYPES"
author: windows-driver-content
description: Specifies the type of a File History backup target.
old-location: winprog\fh_target_drive_types.htm
old-project: DevNotes
ms.assetid: 4D3F3B57-BD6E-4334-8DF6-ECD317A051EC
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: FH_DRIVE_FIXED, FH_DRIVE_REMOTE, FH_DRIVE_REMOVABLE, FH_DRIVE_UNKNOWN, FH_TARGET_DRIVE_TYPES, FH_TARGET_DRIVE_TYPES enumeration [Windows API], _FH_TARGET_DRIVE_TYPES, fhcfg/FH_DRIVE_FIXED, fhcfg/FH_DRIVE_REMOTE, fhcfg/FH_DRIVE_REMOVABLE, fhcfg/FH_DRIVE_UNKNOWN, fhcfg/FH_TARGET_DRIVE_TYPES, winprog.fh_target_drive_types
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FH_TARGET_DRIVE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fhcfg.h
api_name:
-	FH_TARGET_DRIVE_TYPES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# _FH_TARGET_DRIVE_TYPES enumeration


## -description


Specifies the type of a File History backup target.


## -enum-fields




### -field FH_DRIVE_UNKNOWN

The type of the backup target is unknown.


### -field FH_DRIVE_REMOVABLE

The backup target is a locally attached removable storage device, such as a USB thumb drive.


### -field FH_DRIVE_FIXED

The backup target is a locally attached nonremovable storage device, such as an internal hard drive.


### -field FH_DRIVE_REMOTE

The backup target is a storage device that is accessible over network, such as a computer that is running Windows Home Server.


## -see-also




<a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">IFhTarget::GetNumericalProperty</a>
 

 

