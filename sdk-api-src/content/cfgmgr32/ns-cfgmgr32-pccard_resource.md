---
UID: NS:cfgmgr32.PcCard_Resource_s
title: PCCARD_RESOURCE (cfgmgr32.h)
description: The PCCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance.
helpviewer_keywords: ["*PPCCARD_RESOURCE","PCCARD_RESOURCE","PCCARD_RESOURCE structure [Device and Driver Installation]","PPCCARD_RESOURCE","PPCCARD_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/PCCARD_RESOURCE","cfgmgr32/PPCCARD_RESOURCE","cfgmgrst_e644b9fe-478c-4700-b461-1c4dca3c4d10.xml","devinst.pccard_resource"]
old-location: devinst\pccard_resource.htm
tech.root: devinst
ms.assetid: 41f88d8f-2e1d-447d-90e2-6a2a5f7bef6f
ms.date: 12/05/2018
ms.keywords: '*PPCCARD_RESOURCE, PCCARD_RESOURCE, PCCARD_RESOURCE structure [Device and Driver Installation], PPCCARD_RESOURCE, PPCCARD_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/PCCARD_RESOURCE, cfgmgr32/PPCCARD_RESOURCE, cfgmgrst_e644b9fe-478c-4700-b461-1c4dca3c4d10.xml, devinst.pccard_resource'
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
req.typenames: PCCARD_RESOURCE, *PPCCARD_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PcCard_Resource_s
 - cfgmgr32/PcCard_Resource_s
 - PPCCARD_RESOURCE
 - cfgmgr32/PPCCARD_RESOURCE
 - PCCARD_RESOURCE
 - cfgmgr32/PCCARD_RESOURCE
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
 - PCCARD_RESOURCE
---

# PCCARD_RESOURCE structure


## -description

The PCCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field PcCard_Header

A [PCCARD_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-pccard_des) structure.

## -see-also

[PCCARD_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-pccard_des)