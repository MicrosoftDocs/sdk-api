---
UID: NS:winnt._PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
title: "_PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY"
author: windows-sdk-content
description: Used to impose restrictions on what system calls can be invoked by a process.
old-location: base\process_mitigation_system_call_disable_policy.htm
tech.root: ProcThread
ms.assetid: dfcdf4ae-c779-477c-8df6-de24b8037d62
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure, _PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, base.process_mitigation_system_call_disable_policy, winnt/PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, winnt/PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY"
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
 - PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, *PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure


## -description


Used to impose restrictions on what system calls can be invoked by a process.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisallowWin32kSystemCalls

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditDisallowWin32kSystemCalls

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

 




#### - DisallowWin32kSystemCalls : 1

When set to 1, the process is not permitted to perform GUI system calls.


#### - ReservedFlags : 31

This member is reserved for system use.

