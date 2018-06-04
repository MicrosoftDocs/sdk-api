---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


