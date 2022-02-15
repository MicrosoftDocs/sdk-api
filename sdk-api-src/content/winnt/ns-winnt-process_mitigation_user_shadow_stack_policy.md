---
UID: NS:winnt._PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
title: PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
ms.date: 02/21/2021
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
 - _PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - winnt/_PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - PPROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - winnt/PPROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
 - PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY
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

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditBlockNonCetBinaries

If TRUE, binary loads that would have been blocked are instead allowed and diagnostic events are logged in the Event Log.
When this field is TRUE, BlockNonCetBinaries must be TRUE and BlockNonCetBinariesNonEhcont may be TRUE, depending on which types of binaries are currently being blocked from being loaded into the process.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditSetContextIpValidation

If TRUE, Instruction Pointers that would have caused the validation to fail are instead allowed and diagnostic events are logged in the Event Log.
When this field is TRUE, SetContextIpValidation must be TRUE and SetContextIpValidationRelaxedMode may be TRUE, depending on which mode the Instruction Pointer validation is currently operating in.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditUserShadowStack

If TRUE, shadow stack violations that would have been fatal are instead treated as not fatal and diagnostic events are logged in the Event Log.
When this field is TRUE, EnableUserShadowStack must be TRUE and EnableUserShadowStackStrictMode may be TRUE, depending on whether compatibility mode is being audited or strict mode is being audited.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.BlockNonCetBinaries

If TRUE, binaries that are not compiled with CETCOMPAT are blocked from being loaded into the process.
This policy can be enabled after a process has started by calling [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It cannot be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.BlockNonCetBinariesNonEhcont

If TRUE, binaries that are not compiled with CETCOMPAT or do not contain exception handling continuation metadata ([/guard:ehcont](/cpp/build/reference/guard-enable-eh-continuation-metadata)) are blocked from being loaded into the process.
When this field is TRUE, BlockNonCetBinaries must be TRUE.
This policy can be enabled after a process has started by calling [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It cannot be disabled or downgraded once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.CetDynamicApisOutOfProcOnly

If TRUE, certain HSP APIs used to specify security properties of dynamic code can only be called from outside of the process for security purposes.
These APIs are [SetProcessDynamicEHContinuationTargets](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessdynamicehcontinuationtargets) and [SetProcessDynamicEnforcedCetCompatibleRanges](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessdynamicenforcedcetcompatibleranges).
This policy can be enabled after a process has started by calling [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It cannot be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableUserShadowStack

If TRUE, user-mode Hardware-enforced Stack Protection is enabled for the process in compatibility mode.
This means that the CPU verifies function return addresses at runtime by employing a shadow stack mechanism, if supported by the hardware.
In compatibility mode, only shadow stack violations occurring in modules that are considered compatible with shadow stacks (CETCOMPAT) are fatal.
For a module to be considered CETCOMPAT, it needs to be either compiled with [CETCOMPAT](/cpp/build/reference/cetcompat) for binaries, or marked using
[SetProcessDynamicEnforcedCetCompatibleRanges](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessdynamicenforcedcetcompatibleranges) for dynamic code.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableUserShadowStackStrictMode

If TRUE, user-mode Hardware-enforced Stack Protection is enabled for the process in strict mode. All shadow stack violations are fatal.
When this field is TRUE, EnableUserShadowStack must be TRUE.
If HSP is enabled in compatibility mode, it can be upgraded to strict mode at runtime by setting this field to TRUE and calling [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).
HSP cannot be downgraded or disabled via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).
If HSP is disabled, it cannot be enabled via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SetContextIpValidation

If TRUE, when calling APIs that modify the execution context of a thread such as [SetThreadContext](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) and [RtlRestoreContext](/windows/desktop/api/winnt/nf-winnt-rtlrestorecontext), validation is performed on the Instruction Pointer specified in the new execution context.
This field cannot be changed via [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SetContextIpValidationRelaxedMode

If TRUE, the process's Instruction Pointer validation is downgraded to relaxed mode, which allows all Instruction Pointers that are in dynamic code or in binaries that do not contain [exception handling continuation metadata](/cpp/build/reference/guard-enable-eh-continuation-metadata).
When this field is TRUE, SetContextIpValidation must be TRUE.
The process can be upgraded from relaxed mode to normal mode at runtime by setting this field to FALSE and calling [SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.

## -remarks

## -see-also

[CETCOMPAT](/cpp/build/reference/cetcompat)

[GetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)

[SetProcessMitigationPolicy](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)

