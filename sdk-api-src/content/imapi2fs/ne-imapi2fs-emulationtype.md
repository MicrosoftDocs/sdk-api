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

# EmulationType enumeration


## -description


Defines values for media types that the boot image is intended to emulate.


## -enum-fields




### -field EmulationNone

No emulation. The BIOS will not emulate any device type or special sector size for the CD during boot from the CD.


### -field Emulation12MFloppy

Emulates a 1.2 MB floppy disk.


### -field Emulation144MFloppy

Emulates a 1.44 MB floppy disk.


### -field Emulation288MFloppy

Emulates a 2.88 MB floppy disk.


### -field EmulationHardDisk

Emulates a hard disk.


## -remarks



Other values not defined here may exist. Consumers of this enumeration should not presume this list to be the only set of valid values.

For complete details of these emulation types, see the "El Torito" Bootable CD-ROM format specification at  <a href="Http://go.microsoft.com/fwlink/p/?linkid=84155">http://www.phoenix.com/docs/specscdrom.pdf</a>.




## -see-also




<a href="https://msdn.microsoft.com/ade69c2b-ff25-4993-bf4c-ee372e3cc1b0">IBootOptions::get_Emulation</a>



<a href="https://msdn.microsoft.com/93ed301e-fdea-451c-9ab0-6ea9a7fd45de">IBootOptions::put_Emulation</a>
 

 

