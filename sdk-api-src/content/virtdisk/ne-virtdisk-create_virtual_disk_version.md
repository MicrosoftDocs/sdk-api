---
UID: NE:virtdisk._CREATE_VIRTUAL_DISK_VERSION
title: CREATE_VIRTUAL_DISK_VERSION (virtdisk.h)
description: Contains the version of the virtual disk CREATE_VIRTUAL_DISK_PARAMETERS structure to use in calls to virtual disk functions.helpviewer_keywords: ["CREATE_VIRTUAL_DISK_VERSION","CREATE_VIRTUAL_DISK_VERSION enumeration [VHD]","CREATE_VIRTUAL_DISK_VERSION_1","CREATE_VIRTUAL_DISK_VERSION_2","CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED","vdssys/CREATE_VIRTUAL_DISK_VERSION","vdssys/CREATE_VIRTUAL_DISK_VERSION_1","vdssys/CREATE_VIRTUAL_DISK_VERSION_2","vdssys/CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED","vhd.create_virtual_disk_version","virtdisk/CREATE_VIRTUAL_DISK_VERSION","virtdisk/CREATE_VIRTUAL_DISK_VERSION_1","virtdisk/CREATE_VIRTUAL_DISK_VERSION_2","virtdisk/CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED"]
old-location: vhd\create_virtual_disk_version.htm
tech.root: VStor
ms.assetid: 8a9f186a-88aa-43dc-97e0-2ffa43d7ffe5
ms.date: 12/05/2018
ms.keywords: CREATE_VIRTUAL_DISK_VERSION, CREATE_VIRTUAL_DISK_VERSION enumeration [VHD], CREATE_VIRTUAL_DISK_VERSION_1, CREATE_VIRTUAL_DISK_VERSION_2, CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED, vdssys/CREATE_VIRTUAL_DISK_VERSION, vdssys/CREATE_VIRTUAL_DISK_VERSION_1, vdssys/CREATE_VIRTUAL_DISK_VERSION_2, vdssys/CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED, vhd.create_virtual_disk_version, virtdisk/CREATE_VIRTUAL_DISK_VERSION, virtdisk/CREATE_VIRTUAL_DISK_VERSION_1, virtdisk/CREATE_VIRTUAL_DISK_VERSION_2, virtdisk/CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED
f1_keywords:
- virtdisk/CREATE_VIRTUAL_DISK_VERSION
dev_langs:
- c++
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
- VirtDisk.h
- vdssys.h
api_name:
- CREATE_VIRTUAL_DISK_VERSION
targetos: Windows
req.typenames: CREATE_VIRTUAL_DISK_VERSION
req.redist: 
ms.custom: 19H1
---

# CREATE_VIRTUAL_DISK_VERSION enumeration


## -description


Contains the version of the virtual disk 
    <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/ns-virtdisk-create_virtual_disk_parameters">CREATE_VIRTUAL_DISK_PARAMETERS</a> 
    structure to use in calls to virtual disk functions.


## -enum-fields




### -field CREATE_VIRTUAL_DISK_VERSION_UNSPECIFIED

Not supported.


### -field CREATE_VIRTUAL_DISK_VERSION_1

The <b>Version1</b> member structure will be used.


### -field CREATE_VIRTUAL_DISK_VERSION_2

The <b>Version2</b> member structure will be used.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported until Windows 8 and Windows Server 2012.


### -field CREATE_VIRTUAL_DISK_VERSION_3


### -field CREATE_VIRTUAL_DISK_VERSION_4




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
 

 

