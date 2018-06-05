---
UID: NF:wow64apiset.IsWow64GuestMachineSupported
title: IsWow64GuestMachineSupported function
author: windows-sdk-content
description: Determines which architectures are supported (under WOW64) on the given machine architecture.
old-location: base\iswow64guestmachinesupported.htm
old-project: SysInfo
ms.assetid: B6DAAE7A-21B0-475C-AC28-30E83B39F417
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IsWow64GuestMachineSupported, IsWow64GuestMachineSupported function, base.iswow64guestmachinesupported, wow64apiset/IsWow64GuestMachineSupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.lib
-	API-MS-Win-Core-Wow64-L1-1-1.dll
-	KernelBase.dll
api_name:
-	IsWow64GuestMachineSupported
product: Windows
targetos: Windows
req.lib: Kernel32.dll
req.dll: Kernel32.lib
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsWow64GuestMachineSupported function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Determines which architectures are supported (under <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>) on the given machine architecture.


## -parameters




### -param WowGuestMachine [in]

An <a href="https://msdn.microsoft.com/1E5E4F98-925B-424D-9B3D-BC6716FBF990">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.


### -param MachineIsSupported [out]

On success, returns a pointer to a boolean: <b>true</b> if the machine supports WOW64, or <b>false</b> if it does not.


## -returns



On success, returns <b>S_OK</b>; otherwise, returns an error. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>IsWow64GuestMachineSupported</b> is designed for the following scenarios:

<ul>
<li>Debuggers (such as Visual Studio) that want to determine which debugger extensions it needs to install on the system.</li>
<li>Apps that need to determine if <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a> is turned off or not. For example, many apps assume x86-64 systems can always execute x86-32 code at all times, everywhere. Note that this ability does not exist on WinPE or Xbox, and it is an optional component in Server.</li>
<li>Test suites that need to achieve full feature coverage by running tests on all supported architectures in the system. 
</li>
</ul>


