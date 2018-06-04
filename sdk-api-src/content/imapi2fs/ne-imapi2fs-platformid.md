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

# PlatformId enumeration


## -description


Defines values for the operating system architecture that the boot image supports


## -enum-fields




### -field PlatformX86

 Intel Pentium™ series of chip sets. This entry implies a Windows  operating system.


### -field PlatformPowerPC

Apple PowerPC family.


### -field PlatformMac

Apple Macintosh  family.


### -field PlatformEFI

EFI Family.


## -remarks



Other values not defined here may exist. Consumers of this enumeration should not presume this list to be the only set of valid values.




## -see-also




<a href="https://msdn.microsoft.com/8d5ceb0e-4fd2-4146-8e15-b157c80a9d5b">IBootOptions::get_PlatformId</a>



<a href="https://msdn.microsoft.com/295f3a3c-0f01-4b9b-b73c-48f075e6a33a">IBootOptions::put_PlatformId</a>
 

 

