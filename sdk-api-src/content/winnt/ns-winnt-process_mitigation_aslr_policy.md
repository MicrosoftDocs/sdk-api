---
UID: NS:winnt._PROCESS_MITIGATION_ASLR_POLICY
title: PROCESS_MITIGATION_ASLR_POLICY (winnt.h)
description: Contains process mitigation policy settings for Address Space Randomization Layout (ASLR).
helpviewer_keywords: ["*PPROCESS_MITIGATION_ASLR_POLICY","PPROCESS_MITIGATION_ASLR_POLICY","PPROCESS_MITIGATION_ASLR_POLICY structure pointer","PROCESS_MITIGATION_ASLR_POLICY","PROCESS_MITIGATION_ASLR_POLICY structure","_PROCESS_MITIGATION_ASLR_POLICY","base.process_mitigation_aslr_policy","winnt/PPROCESS_MITIGATION_ASLR_POLICY","winnt/PROCESS_MITIGATION_ASLR_POLICY"]
old-location: base\process_mitigation_aslr_policy.htm
tech.root: backup
ms.assetid: 1324d2e7-64a4-45de-856a-30c5c5bf8e7e
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_ASLR_POLICY, PPROCESS_MITIGATION_ASLR_POLICY, PPROCESS_MITIGATION_ASLR_POLICY structure pointer, PROCESS_MITIGATION_ASLR_POLICY, PROCESS_MITIGATION_ASLR_POLICY structure, _PROCESS_MITIGATION_ASLR_POLICY, base.process_mitigation_aslr_policy, winnt/PPROCESS_MITIGATION_ASLR_POLICY, winnt/PROCESS_MITIGATION_ASLR_POLICY'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: PROCESS_MITIGATION_ASLR_POLICY, *PPROCESS_MITIGATION_ASLR_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_ASLR_POLICY
 - winnt/_PROCESS_MITIGATION_ASLR_POLICY
 - PPROCESS_MITIGATION_ASLR_POLICY
 - winnt/PPROCESS_MITIGATION_ASLR_POLICY
 - PROCESS_MITIGATION_ASLR_POLICY
 - winnt/PROCESS_MITIGATION_ASLR_POLICY
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
 - PROCESS_MITIGATION_ASLR_POLICY
---

# PROCESS_MITIGATION_ASLR_POLICY structure


## -description

Contains process mitigation policy settings for Address Space Randomization Layout (ASLR). The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a> functions use this structure.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableBottomUpRandomization

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableForceRelocateImages

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnableHighEntropy

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisallowStrippedImages

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

 




#### - DisallowStrippedImages : 1

Images that have not been built with /DYNAMICBASE and do not have relocation information will fail to load if this flag and <b>EnableForceRelocateImages</b> are set.


#### - EnableBottomUpRandomization : 1

Thread stacks and other bottom-up allocations are subject to randomization by ASLR if this flag is set.  This flag is read-only and cannot be modified after a process has been created.


#### - EnableForceRelocateImages : 1

Images that have not been built with /DYNAMICBASE are forcibly relocated on load if this flag is set.


#### - EnableHighEntropy : 1

Bottom-up allocations are subject to higher degrees of entropy when randomized by ASLR if this flag is set.  This flag only applies to 64-bit processes and is read-only.


#### - ReservedFlags : 28

This member is reserved for system use.