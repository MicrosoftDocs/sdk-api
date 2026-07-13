---
UID: NA:hwreqchkapi
tech.root: hwreqchk
title: hwreqchkapi (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: The hardware requirement evaluator (HWREQCHK) library is a set of APIs that allows callers to get information about a hardware device and determine if the machine is eligible to run a specific version of Windows.
prerelease: true
req.assembly: 
req.construct-type: apiset
req.ddi-compliance: 
req.dll: HWREQCHK.DLL
req.header: hwreqchkapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: HWREQCHK.LIB
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - hwreqchkapi.h
api_name:
 - hwreqchkapi
f1_keywords:
 - hwreqchkapi
 - hwreqchkapi/hwreqchkapi
dev_langs:
 - c++
helpviewer_keywords:
 - hwreqchkapi
---

## -description

The hardware requirement evaluator (HWREQCHK) library is a set of APIs that allows callers to get information about a hardware device and determine if the machine is eligible to run a specific version of Windows 11 (and new versions of the OS as they become available). The API queries various hardware properties and evaluates rules to determine eligibility.

## -remarks

The hardware requirement APIs are a family of APIs used to evaluate a machine/device against the new Windows 11 hardware requirements. It can also be used to determine which of the requirements are not met and what the machine's hardware is currently.

## -see-also
