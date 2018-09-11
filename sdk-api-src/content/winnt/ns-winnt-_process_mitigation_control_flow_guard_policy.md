---
UID: NS:winnt._PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
title: "_PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for Control Flow Guard (CFG).
old-location: base\process_mitigation_control_flow_guard_policy.htm
tech.root: procthread
ms.assetid: AD95D76A-4DDE-4256-B604-15DFD6AD9850
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure pointer, PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure, _PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, base.process_mitigation_control_flow_guard_policy, winnt/PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, winnt/PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY, *PPROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY structure


## -description


Contains process mitigation policy settings for Control Flow Guard (CFG). The <a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a> and <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a> functions use this structure.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableControlFlowGuard

CFG is enabled for the process if this flag is set. This field cannot be changed via <a href="https://msdn.microsoft.com/library/windows/desktop/hh769088%28v=vs.85%29.aspx">SetProcessMitigationPolicy</a>.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableExportSuppression

If TRUE, exported functions will be treated as invalid indirect call targets by default. Exported functions only become valid indirect call targets if they are dynamically resolved via <a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>. This field cannot be changed via <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.StrictMode

If TRUE, all DLLs that are loaded must enable CFG. If a DLL does not enable CFG then the image will fail to load. This policy can be enabled after a process has started by calling <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>. It cannot be disabled once enabled.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.

