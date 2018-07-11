---
UID: NS:virtdisk._STORAGE_DEPENDENCY_INFO_TYPE_1
title: "_STORAGE_DEPENDENCY_INFO_TYPE_1"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) storage dependency information for type 1.
old-location: vhd\storage_dependency_info_type_1.htm
old-project: VStor
ms.assetid: 63296975-583d-415c-8c1f-f0cccfc5a1b3
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PSTORAGE_DEPENDENCY_INFO_TYPE_1, PSTORAGE_DEPENDENCY_INFO_TYPE_1, PSTORAGE_DEPENDENCY_INFO_TYPE_1 structure pointer [VHD], STORAGE_DEPENDENCY_INFO_TYPE_1, STORAGE_DEPENDENCY_INFO_TYPE_1 structure [VHD], _STORAGE_DEPENDENCY_INFO_TYPE_1, vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_1, vdssys/STORAGE_DEPENDENCY_INFO_TYPE_1, vhd.storage_dependency_info_type_1, virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_1, virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: STORAGE_DEPENDENCY_INFO_TYPE_1, *PSTORAGE_DEPENDENCY_INFO_TYPE_1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - STORAGE_DEPENDENCY_INFO_TYPE_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _STORAGE_DEPENDENCY_INFO_TYPE_1 structure


## -description


Contains virtual hard disk (VHD) storage dependency information for type 1.


## -struct-fields




### -field DependencyTypeFlags

A <a href="https://msdn.microsoft.com/f22bcf17-59fd-4a05-9516-2e14f173ed33">DEPENDENT_DISK_FLAG</a> enumeration.


### -field ProviderSpecificFlags

Flags specific to the VHD provider.


### -field VirtualStorageType

A <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

