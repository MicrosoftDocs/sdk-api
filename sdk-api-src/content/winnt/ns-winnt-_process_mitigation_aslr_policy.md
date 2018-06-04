---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

