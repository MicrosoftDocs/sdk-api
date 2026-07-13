---
UID: NS:dxcore_interface.DXCoreFrequencyQueryOutput
title: DXCoreFrequencyQueryOutput
description: Represents the results of a query about the clock frequency of an engine.
ms.date: 10/04/2024
tech.root: dxcore
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dxcore_interface.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcore_interface.h
api_name:
 - DXCoreFrequencyQueryOutput
f1_keywords:
 - DXCoreFrequencyQueryOutput
 - dxcore_interface/DXCoreFrequencyQueryOutput
dev_langs:
 - c++
helpviewer_keywords:
 - DXCoreFrequencyQueryOutput
---

## -description

Represents the results of a query about the clock frequency of an engine.

## -struct-fields

### -field frequency

the clock frequency of an engine (in Hertz).

### -field maxFrequency

the maximum frequency for an engine (in Hertz), without overclocking.

### -field maxOverclockedFrequency

The maximum frequency for an engine (in Hertz), with overclocking.

## -remarks

## -see-also
