---
UID: NF:winbase.SetSystemPowerState
title: SetSystemPowerState function (winbase.h)
author: windows-sdk-content
description: Suspends the system by shutting power down. Depending on the ForceFlag parameter, the function either suspends operation immediately or requests permission from all applications and device drivers before doing so.
old-location: base\setsystempowerstate.htm
tech.root: power
ms.assetid: 58cf4e29-2a2e-499a-85ce-0034f4323cfe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetSystemPowerState, SetSystemPowerState function, _win32_setsystempowerstate, base.setsystempowerstate, winbase/SetSystemPowerState
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - SetSystemPowerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSystemPowerState function


## -description


<p class="CCE_Message">[<b>SetSystemPowerState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/63cb6574-8c0d-4bcb-832c-7088447a5c04">SetSuspendState</a> instead.]

Suspends the system by shutting power down. Depending on the <i>ForceFlag</i> 
    parameter, the function either suspends operation immediately or requests permission from all applications and 
    device drivers before doing so.


## -parameters




### -param fSuspend [in]

If this parameter is <b>TRUE</b>, the system is suspended. If the parameter is 
      <b>FALSE</b>, the system hibernates.


### -param fForce [in]

This parameter has no effect.
	  


## -returns



If power has been suspended and subsequently restored, the return value is nonzero.

If the system was not suspended, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. To enable the 
    <b>SE_SHUTDOWN_NAME</b> privilege, use the 
    <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function. For more 
    information, see <a href="https://msdn.microsoft.com/b8e47d04-07c1-4d57-8209-6b0c397476e5">Changing Privileges in a 
    Token</a>.

If any application or driver denies permission to suspend operation, the function broadcasts a 
    <a href="https://msdn.microsoft.com/0f68628f-9d38-45ca-9487-95bf62075e00">PBT_APMQUERYSUSPENDFAILED</a> event to each 
    application and driver. If power is suspended, this function returns only after system operation is resumed and 
    related <a href="https://msdn.microsoft.com/46452909-ac0e-4c06-8542-0b94d00e6556">WM_POWERBROADCAST</a> messages have been broadcast 
    to all applications and drivers.

This function is similar to the <a href="https://msdn.microsoft.com/63cb6574-8c0d-4bcb-832c-7088447a5c04">SetSuspendState</a> 
    function.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more 
    information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows 
    Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/83cb0fdc-437e-4d03-87f0-6a416281c0d5">PBT_APMQUERYSUSPEND</a>



<a href="https://msdn.microsoft.com/0f68628f-9d38-45ca-9487-95bf62075e00">PBT_APMQUERYSUSPENDFAILED</a>



<a href="https://msdn.microsoft.com/61b177a0-4cff-4740-bed8-a46c06c43be8">PBT_APMSUSPEND</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/63cb6574-8c0d-4bcb-832c-7088447a5c04">SetSuspendState</a>



<a href="https://msdn.microsoft.com/46452909-ac0e-4c06-8542-0b94d00e6556">WM_POWERBROADCAST</a>
 

 

