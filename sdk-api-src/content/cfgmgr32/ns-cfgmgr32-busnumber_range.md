---
UID: NS:cfgmgr32.BusNumber_Range_s
title: BUSNUMBER_RANGE (cfgmgr32.h)
description: The BUSNUMBER_RANGE structure specifies a resource requirements list that describes bus number usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PBUSNUMBER_RANGE","BUSNUMBER_RANGE","BUSNUMBER_RANGE structure [Device and Driver Installation]","PBUSNUMBER_RANGE","PBUSNUMBER_RANGE structure pointer [Device and Driver Installation]","cfgmgr32/BUSNUMBER_RANGE","cfgmgr32/PBUSNUMBER_RANGE","cfgmgrst_6d1e1291-b14d-4eca-9647-014001edd50a.xml","devinst.busnumber_range"]
old-location: devinst\busnumber_range.htm
tech.root: devinst
ms.assetid: 00b9bcd3-f1fe-4853-a6fb-0ac8b1fffa1b
ms.date: 12/05/2018
ms.keywords: '*PBUSNUMBER_RANGE, BUSNUMBER_RANGE, BUSNUMBER_RANGE structure [Device and Driver Installation], PBUSNUMBER_RANGE, PBUSNUMBER_RANGE structure pointer [Device and Driver Installation], cfgmgr32/BUSNUMBER_RANGE, cfgmgr32/PBUSNUMBER_RANGE, cfgmgrst_6d1e1291-b14d-4eca-9647-014001edd50a.xml, devinst.busnumber_range'
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
req.typenames: BUSNUMBER_RANGE, *PBUSNUMBER_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BusNumber_Range_s
 - cfgmgr32/BusNumber_Range_s
 - PBUSNUMBER_RANGE
 - cfgmgr32/PBUSNUMBER_RANGE
 - BUSNUMBER_RANGE
 - cfgmgr32/BUSNUMBER_RANGE
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
 - BUSNUMBER_RANGE
---

# BUSNUMBER_RANGE structure


## -description

The BUSNUMBER_RANGE structure specifies a resource requirements list that describes bus number usage for a device instance. For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field BUSR_Min

The lowest-numbered of a range of contiguous bus numbers that can be allocated to the device.

### -field BUSR_Max

The highest-numbered of a range of contiguous bus numbers that can be allocated to the device.

### -field BUSR_nBusNumbers

The number of contiguous bus numbers required by the device.

### -field BUSR_Flags

<i>Not used.</i>

## -remarks

The BUSNUMBER_RANGE structure is included as a member of the [BUSNUMBER_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_resource) structure.

## -see-also

[BUSNUMBER_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_resource)