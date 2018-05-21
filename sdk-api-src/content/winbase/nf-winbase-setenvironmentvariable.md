---
UID: NF:winbase.SetEnvironmentVariable
title: SetEnvironmentVariable function
author: windows-driver-content
description: Sets the contents of the specified environment variable for the current process.
old-location: base\setenvironmentvariable.htm
old-project: ProcThread
ms.assetid: 95bd6fa5-886d-41dc-a5c3-ede86dbfa15d
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetEnvironmentVariable, SetEnvironmentVariable function, SetEnvironmentVariableA, SetEnvironmentVariableW, _win32_setenvironmentvariable, base.setenvironmentvariable, processenv/SetEnvironmentVariable, processenv/SetEnvironmentVariableA, processenv/SetEnvironmentVariableW, winbase/SetEnvironmentVariable, winbase/SetEnvironmentVariableA, winbase/SetEnvironmentVariableW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetEnvironmentVariableW (Unicode) and SetEnvironmentVariableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	SetEnvironmentVariable
-	SetEnvironmentVariableA
-	SetEnvironmentVariableW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetEnvironmentVariable function


## -description


Sets the contents of the specified environment variable for the current process.


## -parameters




### -param lpName [in]

The name of the environment variable. The operating system creates the environment variable if it does not exist and <i>lpValue</i> is not NULL.


### -param lpValue [in, optional]

The contents of the environment variable. The maximum size of a user-defined environment variable is 32,767 characters. For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543043">Environment Variables</a>.

<b>Windows Server 2003 and Windows XP:  </b>The total size of the environment block for a process may not exceed 32,767 characters.

If this parameter is NULL, the variable is deleted from the current process's environment.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function has no effect on the system environment variables or the environment variables of other processes.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543043">Environment Variables</a>



<a href="https://msdn.microsoft.com/1d4cc328-12e6-4aae-9f58-58675116ad54">GetEnvironmentVariable</a>
 

 

