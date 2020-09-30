---
UID: NS:winnt._PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
title: PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY (winnt.h)
description: Contains process mitigation policy settings for legacy extension point DLLs.
helpviewer_keywords: ["*PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY","PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY","PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure pointer","PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY","PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure","_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY","base.process_mitigation_extension_point_disable_policy","winnt/PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY","winnt/_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY"]
old-location: base\process_mitigation_extension_point_disable_policy.htm
tech.root: backup
ms.assetid: 6B9B5306-F79F-4744-948F-ECBD9EAFC3C3
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure, _PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, base.process_mitigation_extension_point_disable_policy, winnt/PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, winnt/_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY'
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
req.typenames: PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY, *PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
 - winnt/_PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
 - PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
 - winnt/PPROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
 - PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
 - winnt/PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
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
 - PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY
---

# PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY structure


## -description

Contains process mitigation policy settings for legacy extension point DLLs. The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a> functions use this structure.

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