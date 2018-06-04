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
 

 

