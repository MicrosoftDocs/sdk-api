---
UID: NS:winnt._PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
title: PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY (winnt.h)
description: Used to impose restrictions on what system calls can be invoked by a process.
helpviewer_keywords: ["*PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY","PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY","PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure pointer","PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY","PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure","_PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY","base.process_mitigation_system_call_disable_policy","winnt/PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY","winnt/PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY"]
old-location: base\process_mitigation_system_call_disable_policy.htm
tech.root: backup
ms.assetid: dfcdf4ae-c779-477c-8df6-de24b8037d62
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure pointer, PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure, _PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, base.process_mitigation_system_call_disable_policy, winnt/PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, winnt/PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY'
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
req.typenames: PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY, *PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
 - winnt/_PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
 - PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
 - winnt/PPROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
 - PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
 - winnt/PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
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
 - PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY
---

# PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY structure


## -description

Used to impose restrictions on what system calls can be invoked by a process.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

This member is reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisallowWin32kSystemCalls

When set to 1, the process is not permitted to perform GUI system calls.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditDisallowWin32kSystemCalls

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DisallowFsctlSystemCalls

When set to 1, the process is not be able to successfully make NtFsControlFile system calls, with the following FsControlCode exceptions.

- FSCTL_IS_VOLUME_MOUNTED
- FSCTL_PIPE_IMPERSONATE
- FSCTL_PIPE_LISTEN
- FSCTL_PIPE_DISCONNECT
- FSCTL_PIPE_TRANSCEIVE
- FSCTL_PIPE_WAIT
- FSCTL_PIPE_GET_PIPE_ATTRIBUTE
- FSCTL_PIPE_GET_CONNECTION_ATTRIBUTE
- FSCTL_PIPE_GET_HANDLE_ATTRIBUTE
- FSCTL_PIPE_PEEK
- FSCTL_PIPE_EVENT_SELECT
- FSCTL_PIPE_EVENT_ENUM

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditDisallowFsctlSystemCalls

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

This member is reserved for system use.

