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

# tagCOMSD enumeration


## -description


Determines the type of COM security descriptor to get when calling <a href="https://msdn.microsoft.com/8210A6A0-B861-4E85-8E5A-1BF82A01C54E">CoGetSystemSecurityPermissions</a>.


## -enum-fields




### -field SD_LAUNCHPERMISSIONS

Machine-wide launch permissions.


### -field SD_ACCESSPERMISSIONS

Machine-wide access permissions.


### -field SD_LAUNCHRESTRICTIONS

Machine-wide launch limits.


### -field SD_ACCESSRESTRICTIONS

Machine-wide access limits.


## -see-also




<a href="https://msdn.microsoft.com/8210A6A0-B861-4E85-8E5A-1BF82A01C54E">CoGetSystemSecurityPermissions</a>
 

 

