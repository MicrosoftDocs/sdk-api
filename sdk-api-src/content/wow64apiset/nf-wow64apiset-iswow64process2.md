---
UID: NF:wow64apiset.IsWow64Process2
title: IsWow64Process2 function (wow64apiset.h)
description: Determines whether the specified process is running under WOW64; also returns additional machine process and architecture information.
helpviewer_keywords: ["IsWow64Process2","IsWow64Process2 function","base.iswow64process2","wow64apiset/IsWow64Process2"]
old-location: base\iswow64process2.htm
tech.root: fs
ms.assetid: 77B4E3C8-F9DE-4674-9CEA-9C81AEEB393C
ms.date: 12/05/2018
ms.keywords: IsWow64Process2, IsWow64Process2 function, base.iswow64process2, wow64apiset/IsWow64Process2
req.header: wow64apiset.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016, version 1709 [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - IsWow64Process2
 - wow64apiset/IsWow64Process2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - api-ms-win-core-wow64-l1-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Wow64-l1-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - bcrypt.dll
api_name:
 - IsWow64Process2
---

# IsWow64Process2 function


## -description

Determines whether the specified process is running under
<a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>; also returns additional machine process and architecture information.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param pProcessMachine [out]

On success, returns a pointer to an <a href="/windows/desktop/SysInfo/image-file-machine-constants">IMAGE_FILE_MACHINE_*</a> value. The value will be  <b>IMAGE_FILE_MACHINE_UNKNOWN</b> if the target process is not a <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> process; otherwise, it will identify the type of WoW process.

### -param pNativeMachine [out, optional]

On success, returns a pointer to a possible <a href="/windows/desktop/SysInfo/image-file-machine-constants">IMAGE_FILE_MACHINE_*</a> value identifying the native architecture of host system.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>IsWow64Process2</b> provides an improved direct replacement for IsWow64Process. In addition to determining if the specified process is running under <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>, <b>IsWow64Process2</b> returns the following information:

<ul>
<li>Whether the target process, specified by <i>hProcess</i>, is running under Wow or not.</li>
<li>The architecture of the target process.</li>
<li> Optionally, the architecture of the host system.</li>
</ul>
