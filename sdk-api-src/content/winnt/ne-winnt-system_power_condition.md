---
UID: NE:winnt.SYSTEM_POWER_CONDITION
title: SYSTEM_POWER_CONDITION (winnt.h)
description: Used by the GUID_ACDC_POWER_SOURCE power event to indicate the current power source.
helpviewer_keywords: ["PoAc","PoConditionMaximum","PoDc","PoHot","SYSTEM_POWER_CONDITION","SYSTEM_POWER_CONDITION enumeration","base.system_power_condition","winnt/PoAc","winnt/PoConditionMaximum","winnt/PoDc","winnt/PoHot","winnt/SYSTEM_POWER_CONDITION"]
old-location: base\system_power_condition.htm
tech.root: base
ms.assetid: 66636507-466c-43fd-b46c-0b4dddecc15d
ms.date: 12/05/2018
ms.keywords: PoAc, PoConditionMaximum, PoDc, PoHot, SYSTEM_POWER_CONDITION, SYSTEM_POWER_CONDITION enumeration, base.system_power_condition, winnt/PoAc, winnt/PoConditionMaximum, winnt/PoDc, winnt/PoHot, winnt/SYSTEM_POWER_CONDITION
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SYSTEM_POWER_CONDITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYSTEM_POWER_CONDITION
 - winnt/SYSTEM_POWER_CONDITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_POWER_CONDITION
---

# SYSTEM_POWER_CONDITION enumeration


## -description

Used by the <b>GUID_ACDC_POWER_SOURCE</b> power event to indicate the current 
    power source.

## -enum-fields

### -field PoAc

The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive 
      adapter).

### -field PoDc

The system is receiving power from built-in batteries.

### -field PoHot

The computer is powered by a short-term power source such as a UPS device.

### -field PoConditionMaximum

Values equal to or greater than this value indicate an out of range value.

## -see-also

<a href="/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>

