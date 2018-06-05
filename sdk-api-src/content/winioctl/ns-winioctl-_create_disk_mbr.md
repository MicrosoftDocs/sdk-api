---
UID: NS:winioctl._CREATE_DISK_MBR
title: "_CREATE_DISK_MBR"
author: windows-sdk-content
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize master boot record (MBR) disks.
old-location: fs\create_disk_mbr_str.htm
old-project: FileIO
ms.assetid: 6b475622-371d-4097-9de1-6ef31af76322
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PCREATE_DISK_MBR, CREATE_DISK_MBR, CREATE_DISK_MBR structure [Files], PCREATE_DISK_MBR, PCREATE_DISK_MBR structure pointer [Files], _CREATE_DISK_MBR, _win32_create_disk_mbr_str, base.create_disk_mbr_str, fs.create_disk_mbr_str, winioctl/CREATE_DISK_MBR, winioctl/PCREATE_DISK_MBR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: CREATE_DISK_MBR, *PCREATE_DISK_MBR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	CREATE_DISK_MBR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CREATE_DISK_MBR structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize master boot record (MBR) disks.


## -struct-fields




### -field Signature

The disk signature of the MBR disk to be initialized.
					


## -remarks



The 
<b>CREATE_DISK_MBR</b> structure is part of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552484">CREATE_DISK</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552484">CREATE_DISK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552486">CREATE_DISK_GPT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a>
 

 

