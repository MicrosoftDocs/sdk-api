---
UID: NF:winbase.GetStartupInfoA
title: GetStartupInfoA function
author: windows-sdk-content
description: Retrieves the contents of the STARTUPINFO structure that was specified when the calling process was created.
old-location: base\getstartupinfo.htm
old-project: ProcThread
ms.assetid: 191ea201-dc86-4cde-a0cd-be8d2360b22e
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetStartupInfo, GetStartupInfo function, GetStartupInfoA, GetStartupInfoW, _win32_getstartupinfo, base.getstartupinfo, winbase/GetStartupInfo, winbase/GetStartupInfoA, winbase/GetStartupInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetStartupInfoW (Unicode) and GetStartupInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetStartupInfo
 - GetStartupInfoA
 - GetStartupInfoW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetStartupInfoA function


## -description


Retrieves the contents of the 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure that was specified when the calling process was created.


## -parameters




### -param lpStartupInfo [out]

A pointer to a 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure that receives the startup information.


## -returns



This function does not return a value.

If an error occurs, the ANSI version of this function (<b>GetStartupInfoA</b>) can raise an exception. The Unicode version (<b>GetStartupInfoW</b>) does not fail.




## -remarks



The 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure was specified by the process that created the calling process. It can be used to specify properties associated with the main window of the calling process.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>
 

 

