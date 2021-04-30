---
UID: NS:winnt._PROCESS_MITIGATION_DEP_POLICY
title: PROCESS_MITIGATION_DEP_POLICY (winnt.h)
description: Contains process mitigation policy settings for data execution prevention (DEP).
helpviewer_keywords: ["*PPROCESS_MITIGATION_DEP_POLICY","PPROCESS_MITIGATION_DEP_POLICY","PPROCESS_MITIGATION_DEP_POLICY structure pointer","PROCESS_MITIGATION_DEP_POLICY","PROCESS_MITIGATION_DEP_POLICY structure","_PROCESS_MITIGATION_DEP_POLICY","base.process_mitigation_dep_policy","winnt/PPROCESS_MITIGATION_DEP_POLICY","winnt/PROCESS_MITIGATION_DEP_POLICY"]
old-location: base\process_mitigation_dep_policy.htm
tech.root: backup
ms.assetid: 49f257fe-82e2-41b3-b692-9c88d5896273
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_DEP_POLICY, PPROCESS_MITIGATION_DEP_POLICY, PPROCESS_MITIGATION_DEP_POLICY structure pointer, PROCESS_MITIGATION_DEP_POLICY, PROCESS_MITIGATION_DEP_POLICY structure, _PROCESS_MITIGATION_DEP_POLICY, base.process_mitigation_dep_policy, winnt/PPROCESS_MITIGATION_DEP_POLICY, winnt/PROCESS_MITIGATION_DEP_POLICY'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PROCESS_MITIGATION_DEP_POLICY, *PPROCESS_MITIGATION_DEP_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_DEP_POLICY
 - winnt/_PROCESS_MITIGATION_DEP_POLICY
 - PPROCESS_MITIGATION_DEP_POLICY
 - winnt/PPROCESS_MITIGATION_DEP_POLICY
 - PROCESS_MITIGATION_DEP_POLICY
 - winnt/PROCESS_MITIGATION_DEP_POLICY
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
 - PROCESS_MITIGATION_DEP_POLICY
---

# PROCESS_MITIGATION_DEP_POLICY structure


## -description

Contains process mitigation policy settings for data execution prevention (DEP). The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a> functions use this structure.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Enable

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisableAtlThunkEmulation

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

### -field Permanent

DEP is permanently enabled and cannot be disabled if this field is set to TRUE.


#### - DisableAtlThunkEmulation : 1

ATL thunk emulation is disabled for the process if this flag is set.


#### - Enable : 1

DEP is enabled for the process if this flag is set.


#### - ReservedFlags : 30

This member is reserved for system use.