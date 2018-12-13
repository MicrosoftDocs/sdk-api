---
UID: NS:winnt._PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY
title: PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY
author: windows-sdk-content
description: Used to impose new behavior on handle references that are not valid.
old-location: base\process_mitigation_strict_handle_check_policy.htm
tech.root: procthread
ms.assetid: 32d97712-67fe-44f2-92d8-23855db5502d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, PPROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, PPROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY structure pointer, PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY structure, _PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, base.process_mitigation_strict_handle_check_policy, winnt/PPROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, winnt/PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY, *PPROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY
req.redist: 
---

# PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY structure


## -description


Used to impose new behavior on handle references that are not valid.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.RaiseExceptionOnInvalidHandleReference

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.HandleExceptionsPermanentlyEnabled

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

 




#### - HandleExceptionsPermanentlyEnabled : 1

When set to 1, exceptions for invalid kernel handles are permanently enabled.


#### - RaiseExceptionOnInvalidHandleReference : 1

When set to 1, an exception is raised if an invalid handle to a kernel object is used. Except as noted in the Remarks section, once exceptions for invalid handles are enabled for a process, they cannot be disabled.


#### - ReservedFlags : 30

This member is reserved for system use.


## -remarks



As a general rule, strict handle checking cannot be turned off once it is turned on. Therefore, when calling the <a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a> function with this policy, the values of the <b>RaiseExceptionOnInvalidHandleReference</b> and <b>HandleExceptionsPermanentlyEnabled</b> substructure members must be the same. It is not possible to enable invalid handle exceptions only temporarily.

The exception to the general rule about strict handle checking always being a permanent state is that debugging tools such as Application Verifier can cause the operating system to enable invalid handle exceptions temporarily. Under those cases, it is possible for the <a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a> function to return with <b>RaiseExceptionOnInvalidHandleReference</b> set to 1, but <b>HandleExceptionsPermanentlyEnabled</b> set to 0.



