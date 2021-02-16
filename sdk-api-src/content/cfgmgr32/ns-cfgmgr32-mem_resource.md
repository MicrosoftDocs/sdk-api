---
UID: NS:cfgmgr32.Mem_Resource_s
title: MEM_RESOURCE (cfgmgr32.h)
description: The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PMEM_RESOURCE","MEM_RESOURCE","MEM_RESOURCE structure [Device and Driver Installation]","PMEM_RESOURCE","PMEM_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/MEM_RESOURCE","cfgmgr32/PMEM_RESOURCE","cfgmgrst_ab2f2f67-e38b-45b4-9b63-617d730f8cc8.xml","devinst.mem_resource"]
old-location: devinst\mem_resource.htm
tech.root: devinst
ms.assetid: 42ecd736-abd3-4ac8-82bb-6bb69af1d96d
ms.date: 12/05/2018
ms.keywords: '*PMEM_RESOURCE, MEM_RESOURCE, MEM_RESOURCE structure [Device and Driver Installation], PMEM_RESOURCE, PMEM_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/MEM_RESOURCE, cfgmgr32/PMEM_RESOURCE, cfgmgrst_ab2f2f67-e38b-45b4-9b63-617d730f8cc8.xml, devinst.mem_resource'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MEM_RESOURCE, *PMEM_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Mem_Resource_s
 - cfgmgr32/Mem_Resource_s
 - PMEM_RESOURCE
 - cfgmgr32/PMEM_RESOURCE
 - MEM_RESOURCE
 - cfgmgr32/MEM_RESOURCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - MEM_RESOURCE
---

# MEM_RESOURCE structure


## -description

The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field MEM_Header

A [MEM_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_des) structure.

### -field MEM_Data

#### For a resource list:

Zero.



#### For a resource requirements list:

A [MEM_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_range) array.

## -see-also

[MEM_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_des)



[MEM_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_range)