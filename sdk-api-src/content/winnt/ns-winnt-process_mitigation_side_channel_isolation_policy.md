---
UID: NS:winnt._PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
title: PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY (winnt.h)
description: This data structure provides the status of process policies that are related to the mitigation of side channels. This can include side channel attacks involving speculative execution and page combining.
helpviewer_keywords: ["*PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY","PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY","PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY structure pointer","PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY","PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY structure","_PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY","base.process_mitigation_side_channel_isolation_policy","winnt/PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY","winnt/PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY"]
old-location: base\process_mitigation_side_channel_isolation_policy.htm
tech.root: backup
ms.assetid: FEF2884D-7FE4-4DA7-AC2D-822FFACD4D7B
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY structure pointer, PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY structure, _PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, base.process_mitigation_side_channel_isolation_policy, winnt/PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, winnt/PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY'
req.header: winnt.h
req.include-header: 
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
req.typenames: PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY, *PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
 - winnt/_PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
 - PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
 - winnt/PPROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
 - PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
 - winnt/PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY
---

## -description

This data structure provides the status of process policies that are related to the mitigation of side channels. This can include side channel attacks involving speculative execution and page combining.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SmtBranchTargetIsolation

If **TRUE** then, while this process is executing in user-mode, requests the application of hardware mitigations to prevent cross-SMT-thread branch target pollution.

If the hardware doesn't provide support for such a mitigation, or the mitigation has been disabled system-wide, then this policy has no effect.

To enable this policy after a process has started, you can call [SetProcessMitigationPolicy](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It can't be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsolateSecurityDomain

If **TRUE**, isolates this process into a distinct security domain, even from other processes running as the same security context. That prevents branch target injection cross-process.

Page-combining is limited to processes within the same security domain. This flag effectively limits the process to only combining internally to the process itself, except for common pages and unless further restricted by the **DisablePageCombine** policy.

To enable this policy after a process has started, you can call [SetProcessMitigationPolicy](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It can't be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisablePageCombine

If **TRUE**, disables all page-combining for this process, even internally to the process itself, except for common pages (pages of entirely 0s or entirely 1s).

To enable this policy after a process has started, you can call [SetProcessMitigationPolicy](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It can't be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SpeculativeStoreBypassDisable

If **TRUE** then, while this process is executing in user-mode, and in order to mitigate intra-process SSB, requests that hardware mitigations for Speculative Store Bypass (SSB) be enabled.

If the hardware doesn't provide support for such a mitigation, or the mitigation has been disabled system-wide, then this policy has no effect.

To enable this policy after a process has started, you can call [SetProcessMitigationPolicy](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It can't be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.RestrictCoreSharing

If **TRUE**, the CPU scheduler prevents threads within this process from being scheduled to the same core as threads from another security domain.

This policy can't be enabled on systems where the scheduler is incapable of providing this guarantee. For example, this policy can't be enabled for processes in a virtual machine unless the hypervisor reports the absence of [non-architectural core sharing](/windows-server/virtualization/hyper-v/manage/about-hyper-v-scheduler-type-selection#nononarchitecturalcoresharing-enlightenment-details).

To enable this policy after a process has started, you can call [SetProcessMitigationPolicy](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy). It can't be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.
