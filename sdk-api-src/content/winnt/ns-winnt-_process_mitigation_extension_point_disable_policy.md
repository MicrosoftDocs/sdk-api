---
UID: NS:winnt._PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
title: "_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for legacy extension point DLLs.
old-location: base\process_mitigation_extension_point_disable_policy.htm
tech.root: procthread
ms.assetid: 6B9B5306-F79F-4744-948F-ECBD9EAFC3C3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure, _PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, base.process_mitigation_extension_point_disable_policy, winnt/PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, winnt/_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, *PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure


## -description


Contains process mitigation policy settings for legacy extension point DLLs. The <a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a> and <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a> functions use this structure.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisableExtensionPoints

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

 




#### - DisableExtensionPoints : 1

Prevents legacy extension point DLLs from being loaded into the process.


#### - ReservedFlags : 31

This member is reserved for system use.

