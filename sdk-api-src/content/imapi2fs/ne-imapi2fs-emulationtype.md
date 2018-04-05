---
UID: NE:imapi2fs.EmulationType
title: EmulationType
author: windows-driver-content
description: Defines values for media types that the boot image is intended to emulate.
old-location: imapi\emulationtype.htm
old-project: imapi
ms.assetid: 53e87d6d-9547-4437-9548-652cfcbd308e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Emulation12MFloppy, Emulation144MFloppy, Emulation288MFloppy, EmulationHardDisk, EmulationNone, EmulationType, EmulationType enumeration [IMAPI], imapi.emulationtype, imapi2fs/Emulation12MFloppy, imapi2fs/Emulation144MFloppy, imapi2fs/Emulation288MFloppy, imapi2fs/EmulationHardDisk, imapi2fs/EmulationNone, imapi2fs/EmulationType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EmulationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	imapi2fs.h
api_name:
-	EmulationType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

