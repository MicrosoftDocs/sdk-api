---
UID: NS:winioctl._CREATE_DISK_MBR
title: CREATE_DISK_MBR
author: windows-sdk-content
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize master boot record (MBR) disks.
old-location: fs\create_disk_mbr_str.htm
tech.root: FileIO
ms.assetid: 6b475622-371d-4097-9de1-6ef31af76322
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCREATE_DISK_MBR, CREATE_DISK_MBR, CREATE_DISK_MBR structure [Files], PCREATE_DISK_MBR, PCREATE_DISK_MBR structure pointer [Files], _win32_create_disk_mbr_str, base.create_disk_mbr_str, fs.create_disk_mbr_str, winioctl/CREATE_DISK_MBR, winioctl/PCREATE_DISK_MBR"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CREATE_DISK_MBR
product: Windows
targetos: Windows
req.typenames: CREATE_DISK_MBR, *PCREATE_DISK_MBR
req.redist: 
---

# CREATE_DISK_MBR structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize master boot record (MBR) disks.


## -struct-fields




### -field Signature

The disk signature of the MBR disk to be initialized.
					


## -remarks



The 
<b>CREATE_DISK_MBR</b> structure is part of the 
<a href="https://msdn.microsoft.com/ec4a1ef9-ff2e-41b3-951b-241c545f256b">CREATE_DISK</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ec4a1ef9-ff2e-41b3-951b-241c545f256b">CREATE_DISK</a>



<a href="https://msdn.microsoft.com/526a265b-e15e-4cd2-adaf-c955a8cb92e5">CREATE_DISK_GPT</a>



<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a>
 

 

