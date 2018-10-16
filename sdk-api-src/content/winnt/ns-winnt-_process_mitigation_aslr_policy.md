---
UID: NS:winnt._PROCESS_MITIGATION_ASLR_POLICY
title: "_PROCESS_MITIGATION_ASLR_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for Address Space Randomization Layout (ASLR).
old-location: base\process_mitigation_aslr_policy.htm
tech.root: procthread
ms.assetid: 1324d2e7-64a4-45de-856a-30c5c5bf8e7e
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PPROCESS_MITIGATION_ASLR_POLICY, PPROCESS_MITIGATION_ASLR_POLICY, PPROCESS_MITIGATION_ASLR_POLICY structure pointer, PROCESS_MITIGATION_ASLR_POLICY, PROCESS_MITIGATION_ASLR_POLICY structure, _PROCESS_MITIGATION_ASLR_POLICY, base.process_mitigation_aslr_policy, winnt/PPROCESS_MITIGATION_ASLR_POLICY, winnt/PROCESS_MITIGATION_ASLR_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_ASLR_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_ASLR_POLICY, *PPROCESS_MITIGATION_ASLR_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_ASLR_POLICY structure


## -description


Contains process mitigation policy settings for Address Space Randomization Layout (ASLR). The <a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a> and <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a> functions use this structure.


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

