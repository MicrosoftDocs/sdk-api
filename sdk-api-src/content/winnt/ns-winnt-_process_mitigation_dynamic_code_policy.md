---
UID: NS:winnt._PROCESS_MITIGATION_DYNAMIC_CODE_POLICY
title: "_PROCESS_MITIGATION_DYNAMIC_CODE_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for restricting dynamic code generation and modification.
old-location: base\process_mitigation_dynamic_code_policy.htm
tech.root: procthread
ms.assetid: 7BEFC437-FFE4-4971-8D99-E31D102376D4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPROCESS_MITIGATION_DYNAMIC_CODE_POLICY, PPROCESS_MITIGATION_DYNAMIC_CODE_POLICY, PPROCESS_MITIGATION_DYNAMIC_CODE_POLICY structure pointer, PROCESS_MITIGATION_DYNAMIC_CODE_POLICY, PROCESS_MITIGATION_DYNAMIC_CODE_POLICY structure, _PROCESS_MITIGATION_DYNAMIC_CODE_POLICY, base.process_mitigation_dynamic_code_policy, winnt/PPROCESS_MITIGATION_DYNAMIC_CODE_POLICY, winnt/PROCESS_MITIGATION_DYNAMIC_CODE_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PROCESS_MITIGATION_DYNAMIC_CODE_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_DYNAMIC_CODE_POLICY, *PPROCESS_MITIGATION_DYNAMIC_CODE_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_DYNAMIC_CODE_POLICY structure


## -description


Contains process mitigation policy settings for restricting dynamic code generation and modification.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

Reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ProhibitDynamicCode

Set (0x1) to prevent the process from generating dynamic code or modifying existing executable code; otherwise leave unset (0x0).


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AllowThreadOptOut

Set (0x1) to allow threads to opt out of the restrictions on dynamic code generation by calling the <a href="https://msdn.microsoft.com/c0159bea-870a-46b7-a350-91fe52efae49">SetThreadInformation</a> function with the <i>ThreadInformation</i> parameter set to <b>ThreadDynamicCodePolicy</b>; otherwise leave unset (0x0). You should not use the <b>AllowThreadOptOut</b> and <b>ThreadDynamicCodePolicy</b> settings together to provide strong security. These settings are only intended to enable applications to adapt their code more easily for full dynamic code restrictions. 



### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AllowRemoteDowngrade

Set (0x1) to allow non-AppContainer processes to modify all of the dynamic code settings for the calling process, including relaxing dynamic code restrictions after they have been set.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditProhibitDynamicCode

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

Reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a>



<a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>
 

 

