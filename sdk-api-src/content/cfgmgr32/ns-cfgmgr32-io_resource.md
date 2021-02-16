---
UID: NS:cfgmgr32.IO_Resource_s
title: IO_RESOURCE (cfgmgr32.h)
description: The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance.
helpviewer_keywords: ["*PIO_RESOURCE","IO_RESOURCE","IO_RESOURCE structure [Device and Driver Installation]","PIO_RESOURCE","PIO_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/IO_RESOURCE","cfgmgr32/PIO_RESOURCE","cfgmgrst_4016b1e2-26af-4ccb-b2d9-823e0c4bf66c.xml","devinst.io_resource"]
old-location: devinst\io_resource.htm
tech.root: devinst
ms.assetid: d18a1f92-b76c-4240-9a0e-7474c258436c
ms.date: 12/05/2018
ms.keywords: '*PIO_RESOURCE, IO_RESOURCE, IO_RESOURCE structure [Device and Driver Installation], PIO_RESOURCE, PIO_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IO_RESOURCE, cfgmgr32/PIO_RESOURCE, cfgmgrst_4016b1e2-26af-4ccb-b2d9-823e0c4bf66c.xml, devinst.io_resource'
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
req.typenames: IO_RESOURCE, *PIO_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IO_Resource_s
 - cfgmgr32/IO_Resource_s
 - PIO_RESOURCE
 - cfgmgr32/PIO_RESOURCE
 - IO_RESOURCE
 - cfgmgr32/IO_RESOURCE
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
 - IO_RESOURCE
---

# IO_RESOURCE structure


## -description

The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IO_Header

An [IO_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_des) structure.

### -field IO_Data

#### For a resource list:

Zero.



#### For a resource requirements list:

An [IO_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_range) array.

## -see-also

[IO_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_des)



[IO_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_range)