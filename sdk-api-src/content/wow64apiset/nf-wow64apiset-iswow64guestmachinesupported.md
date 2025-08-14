---
UID: NF:wow64apiset.IsWow64GuestMachineSupported
title: IsWow64GuestMachineSupported function (wow64apiset.h)
description: Determines which architectures are supported (under WOW64) on the given machine architecture.
helpviewer_keywords: ["IsWow64GuestMachineSupported","IsWow64GuestMachineSupported function","base.iswow64guestmachinesupported","wow64apiset/IsWow64GuestMachineSupported"]
old-location: base\iswow64guestmachinesupported.htm
tech.root: fs
ms.assetid: B6DAAE7A-21B0-475C-AC28-30E83B39F417
ms.date: 12/05/2018
ms.keywords: IsWow64GuestMachineSupported, IsWow64GuestMachineSupported function, base.iswow64guestmachinesupported, wow64apiset/IsWow64GuestMachineSupported
req.header: wow64apiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
req.lib: Kernel32.dll
req.dll: Kernel32.lib
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsWow64GuestMachineSupported
 - wow64apiset/IsWow64GuestMachineSupported
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
 - kernel32.lib
 - API-MS-Win-Core-Wow64-L1-1-1.dll
 - KernelBase.dll
api_name:
 - IsWow64GuestMachineSupported
---

# IsWow64GuestMachineSupported function

## -description

Determines which architectures are supported (under <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>) on the given machine architecture.

## -parameters

### -param WowGuestMachine [in]

An <a href="/windows/desktop/SysInfo/image-file-machine-constants">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.

### -param MachineIsSupported [out]

On success, returns a pointer to a boolean: <b>true</b> if the machine supports WOW64, or <b>false</b> if it does not.

## -returns

On success, returns <b>S_OK</b>; otherwise, returns an error. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>IsWow64GuestMachineSupported</b> is designed for the following scenarios:

<ul>
<li>Debuggers (such as Visual Studio) that want to determine which debugger extensions it needs to install on the system.</li>
<li>Apps that need to determine if <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> is turned off or not. For example, many apps assume x86-64 systems can always execute x86-32 code at all times, everywhere. Note that this ability does not exist on WinPE or Xbox, and it is an optional component in Server.</li>
<li>Test suites that need to achieve full feature coverage by running tests on all supported architectures in the system. 
</li>
</ul>