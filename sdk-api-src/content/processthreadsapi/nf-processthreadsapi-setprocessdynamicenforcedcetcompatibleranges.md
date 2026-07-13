---
UID: NF:processthreadsapi.SetProcessDynamicEnforcedCetCompatibleRanges
tech.root: processthreadsapi
title: SetProcessDynamicEnforcedCetCompatibleRanges
ms.date: 02/02/2021
ms.topic: language-reference
targetos: Windows
description: Sets dynamic enforced CETCOMPAT ranges for the specified process.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041.662)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041.662)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - processthreadsapi.h
api_name:
 - SetProcessDynamicEnforcedCetCompatibleRanges
f1_keywords:
 - SetProcessDynamicEnforcedCetCompatibleRanges
 - processthreadsapi/SetProcessDynamicEnforcedCetCompatibleRanges
dev_langs:
 - c++
---

## -description

> [!NOTE]
> This API was added to the 19041 SDK in an update released in November 2020.

Sets dynamic enforced CETCOMPAT ranges for the specified process.

## -parameters

### -param Process

A handle to the process. This handle must have the <b>PROCESS_SET_INFORMATION</b> access right. 
For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param NumberOfRanges

Supplies the number of dynamic enforced CETCOMPAT ranges to set.

### -param Ranges

A pointer to an array of dynamic enforced CETCOMPAT ranges. For more information on this structure, see <a href="/windows/win32/api/winnt/ns-winnt-process_dynamic_enforced_address_range">PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
Note that even if the function fails, a portion of the supplied CETCOMPAT ranges may have been successfully processed.
The caller needs to check the flags in each individual CETCOMPAT range specified via <i>Ranges</i> to determine if it was successfully processed.

## -remarks

User-mode Hardware-enforced Stack Protection (HSP) is a security feature where the CPU verifies function return addresses at runtime by employing a shadow stack mechanism, if supported by the hardware.
In HSP compatibility mode, only shadow stack violations occurring in modules that are considered compatible with shadow stacks (CETCOMPAT) are fatal.
For a module to be considered CETCOMPAT, it needs to be either compiled with [CETCOMPAT](/cpp/build/reference/cetcompat) for binaries, or marked using <i>SetProcessDynamicEnforcedCetCompatibleRanges</i> for dynamic code.
In HSP strict mode, all shadow stack violations are fatal.

## -see-also

