---
UID: NS:cfgmgr32.MfCard_Resource_s
title: MFCARD_RESOURCE (cfgmgr32.h)
description: The MFCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by one of the hardware functions provided by an instance of a multifunction device.
helpviewer_keywords: ["*PMFCARD_RESOURCE","MFCARD_RESOURCE","MFCARD_RESOURCE structure [Device and Driver Installation]","PMFCARD_RESOURCE","PMFCARD_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/MFCARD_RESOURCE","cfgmgr32/PMFCARD_RESOURCE","cfgmgrst_bb72fc57-6d43-447c-8995-1cb7649914af.xml","devinst.mfcard_resource"]
old-location: devinst\mfcard_resource.htm
tech.root: devinst
ms.assetid: 26dbefb6-bc5c-4060-902d-3fd1adf833cb
ms.date: 12/05/2018
ms.keywords: '*PMFCARD_RESOURCE, MFCARD_RESOURCE, MFCARD_RESOURCE structure [Device and Driver Installation], PMFCARD_RESOURCE, PMFCARD_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/MFCARD_RESOURCE, cfgmgr32/PMFCARD_RESOURCE, cfgmgrst_bb72fc57-6d43-447c-8995-1cb7649914af.xml, devinst.mfcard_resource'
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
req.typenames: MFCARD_RESOURCE, *PMFCARD_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MfCard_Resource_s
 - cfgmgr32/MfCard_Resource_s
 - PMFCARD_RESOURCE
 - cfgmgr32/PMFCARD_RESOURCE
 - MFCARD_RESOURCE
 - cfgmgr32/MFCARD_RESOURCE
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
 - MFCARD_RESOURCE
---

# MFCARD_RESOURCE structure


## -description

The MFCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <i>one</i> of the hardware functions provided by an instance of a multifunction device. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field MfCard_Header

A [MFCARD_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mfcard_des) structure.

## -see-also

[MFCARD_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mfcard_des)