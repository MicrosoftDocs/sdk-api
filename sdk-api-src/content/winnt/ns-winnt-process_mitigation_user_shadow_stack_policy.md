---
UID: NS:winnt._PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
title: PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
ms.date: 4/28/2020
ms.topic: language-reference
targetos: Windows
description: Contains process mitigation policy settings for user-mode Hardware-enforced Stack Protection (HSP).
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY, *PPROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
f1_keywords:
 - winnt/_PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - winnt/PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
dev_langs:
 - c++
---

## -description

Contains process mitigation policy settings for user-mode Hardware-enforced Stack Protection (HSP). The [GetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy) and [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy) functions use this structure.


## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableUserShadowStack

If TRUE, user-mode Hardware-enforced Stack Protection is enabled for the process in compatibility mode.
This means that the CPU verifies function return addresses at runtime by employing a shadow stack mechanism, if supported by the hardware.
In compatibility mode, only shadow stack violations occurring in modules compiled with [CETCOMPAT](/cpp/build/reference/cetcompat) are fatal.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.


## -remarks

## -see-also
[CETCOMPAT](/cpp/build/reference/cetcompat)

[GetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)

[SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)
