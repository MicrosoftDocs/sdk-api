---
UID: NS:presentationtypes.SystemInterruptTime
tech.root: comp_swapchain
title: SystemInterruptTime
ms.date: 06/08/2021
targetos: Windows
description: Represents the amount of time since the system was last started, in 100ns intervals.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: presentationtypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: SystemInterruptTime
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentationtypes.h
api_name:
 - SystemInterruptTime
f1_keywords:
 - SystemInterruptTime
 - presentationtypes/SystemInterruptTime
dev_langs:
 - c++
---

## -description

Represents the amount of time since the system was last started, in 100ns intervals.

## -struct-fields

### -field value

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**

The amount of time since the system was last started, in 100ns intervals.

## -remarks

## -see-also

[Interrupt Time](/windows/win32/sysinfo/interrupt-time), [IPresentationManager::SetTargetTime](../presentation/nf-presentation-ipresentationmanager-settargettime.md)
