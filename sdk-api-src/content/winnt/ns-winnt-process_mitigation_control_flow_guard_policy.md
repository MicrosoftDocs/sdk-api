---
UID: NS:winnt._PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
title: PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY (winnt.h)
description: Contains process mitigation policy settings for Control Flow Guard (CFG).
helpviewer_keywords: ["*PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY","PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY","PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure pointer","PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY","PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure","_PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY","base.process_mitigation_control_flow_guard_policy","winnt/PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY","winnt/PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY"]
old-location: base\process_mitigation_control_flow_guard_policy.htm
tech.root: backup
ms.assetid: AD95D76A-4DDE-4256-B604-15DFD6AD9850
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure pointer, PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure, _PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, base.process_mitigation_control_flow_guard_policy, winnt/PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, winnt/PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, *PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
 - winnt/_PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
 - PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
 - winnt/PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
 - PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
 - winnt/PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
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
 - PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
---

# PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure


## -description

Contains process mitigation policy settings for Control Flow Guard (CFG). The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a> functions use this structure.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableControlFlowGuard

CFG is enabled for the process if this flag is set. This field cannot be changed via <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a>.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableExportSuppression

If TRUE, exported functions will be treated as invalid indirect call targets by default. Exported functions only become valid indirect call targets if they are dynamically resolved via <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. This field cannot be changed via <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a>.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.StrictMode

If TRUE, all DLLs that are loaded must enable CFG. If a DLL does not enable CFG then the image will fail to load. This policy can be enabled after a process has started by calling <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a>. It cannot be disabled once enabled.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.