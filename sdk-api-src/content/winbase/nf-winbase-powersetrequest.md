---
UID: NF:winbase.PowerSetRequest
title: PowerSetRequest function
author: windows-sdk-content
description: Increments the count of power requests of the specified type for a power request object.
old-location: base\powersetrequest.htm
old-project: Power
ms.assetid: 85249de8-5832-4f25-bbd9-3576cfd1caa0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PowerRequestAwayModeRequired, PowerRequestDisplayRequired, PowerRequestExecutionRequired, PowerRequestSystemRequired, PowerSetRequest, PowerSetRequest function, base.powersetrequest, winbase/PowerSetRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - PowerSetRequest
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PowerSetRequest function


## -description


Increments the count of power requests of the specified type for a power request object.


## -parameters




### -param PowerRequest [in]

A handle to a power request object.


### -param RequestType [in]

The power request type to be incremented. This parameter can be one of the following values.



#### PowerRequestDisplayRequired

The display remains on even if there is no user input for an extended period of time.



#### PowerRequestSystemRequired

The system continues to run instead of entering sleep after a period of user inactivity. 
                                



#### PowerRequestAwayModeRequired

The system enters away mode instead of sleep in response to explicit action by the user. In away mode, the system continues to run but turns off audio and video to give the appearance of sleep.



#### PowerRequestExecutionRequired

The calling process continues to run instead of being suspended or terminated by process lifetime management mechanisms. When and how long the process is allowed to run depends on the operating system and  power policy settings.

                                

On systems not capable of connected standby, an active <b>PowerRequestExecutionRequired</b> request implies <b>PowerRequestSystemRequired</b>.

<div class="alert"><b>Note</b>  <b>PowerRequestExecutionRequired</b> is supported starting with Windows 8 and Windows Server 2012.</div>
<div> </div>

## -returns



If the function succeeds, it returns a nonzero value.
                    
                        

If the function fails, it returns zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To conserve power and provide the best user experience, applications that use power requests should follow these best practices:
            
                

<ul>
<li>When creating a power request, provide a localized text string that describes the reason for the request in the <a href="https://msdn.microsoft.com/006bb84f-5e51-4f6e-8a44-6b50e763c5ca">REASON_CONTEXT</a> structure.</li>
<li>Call <b>PowerSetRequest</b> immediately before the scenario that requires the request.</li>
<li>Call <a href="https://msdn.microsoft.com/794248b1-5aa8-495e-aca6-1a1f35dc9c7f">PowerClearRequest</a> to decrement the reference count for the request as soon as the scenario is finished.</li>
<li>Clean up all request objects and associated handles before the process exits or the service stops.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/794248b1-5aa8-495e-aca6-1a1f35dc9c7f">PowerClearRequest</a>



<a href="https://msdn.microsoft.com/2122bf00-9e6b-48ab-89b0-f53dd6804902">PowerCreateRequest</a>
 

 

