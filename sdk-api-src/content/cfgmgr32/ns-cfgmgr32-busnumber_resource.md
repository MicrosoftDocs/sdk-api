---
UID: NS:cfgmgr32.BusNumber_Resource_s
title: BUSNUMBER_RESOURCE (cfgmgr32.h)
description: The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PBUSNUMBER_RESOURCE","BUSNUMBER_RESOURCE","BUSNUMBER_RESOURCE structure [Device and Driver Installation]","PBUSNUMBER_RESOURCE","PBUSNUMBER_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/BUSNUMBER_RESOURCE","cfgmgr32/PBUSNUMBER_RESOURCE","cfgmgrst_5fb3a498-87c1-40c1-8169-4348f2fabe03.xml","devinst.busnumber_resource"]
old-location: devinst\busnumber_resource.htm
tech.root: devinst
ms.assetid: 8dbf5499-8e43-4db9-b0ec-6536f1c6121c
ms.date: 12/05/2018
ms.keywords: '*PBUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE, BUSNUMBER_RESOURCE structure [Device and Driver Installation], PBUSNUMBER_RESOURCE, PBUSNUMBER_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/BUSNUMBER_RESOURCE, cfgmgr32/PBUSNUMBER_RESOURCE, cfgmgrst_5fb3a498-87c1-40c1-8169-4348f2fabe03.xml, devinst.busnumber_resource'
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
req.typenames: BUSNUMBER_RESOURCE, *PBUSNUMBER_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BusNumber_Resource_s
 - cfgmgr32/BusNumber_Resource_s
 - PBUSNUMBER_RESOURCE
 - cfgmgr32/PBUSNUMBER_RESOURCE
 - BUSNUMBER_RESOURCE
 - cfgmgr32/BUSNUMBER_RESOURCE
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
 - BUSNUMBER_RESOURCE
---

# BUSNUMBER_RESOURCE structure


## -description

The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field BusNumber_Header

A [BUSNUMBER_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_des) structure.

### -field BusNumber_Data

#### For a resource list:

Zero.



#### For a resource requirements list:

A [BUSNUMBER_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_range) array.

## -see-also

[BUSNUMBER_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_des)



[BUSNUMBER_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_range)