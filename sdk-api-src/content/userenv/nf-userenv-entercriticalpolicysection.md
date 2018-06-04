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

# EnterCriticalPolicySection function


## -description


The 
    <b>EnterCriticalPolicySection</b> function pauses the application of policy to allow applications to safely read policy settings. Applications  call this function if they read multiple policy entries and must ensure that the settings are not changed while they are being read. This mutex protects Group Policy processing for all client-side extensions stored in a Group Policy Object (GPO).


## -parameters




### -param bMachine [in]

A value that specifies whether to stop the application of computer policy or user policy. If this value is <b>TRUE</b>, the system stops applying computer policy. If this value is <b>FALSE</b>, the system stops applying user policy.


## -returns



If the function succeeds, the return value is a handle to a policy section.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The maximum amount of time an application can hold a critical section is 10 minutes. After 10 minutes, the system releases the critical section and policy can be applied again.

To acquire both the computer and user critical section objects, acquire the user critical section object before acquiring the computer critical section object. This will help prevent a deadlock situation.

To close the handle, call the 
<a href="https://msdn.microsoft.com/9e6a938f-c9cb-4baf-b7d0-4316e45f874c">LeaveCriticalPolicySection</a> function. The policy section handle cannot be used in any other Windows functions.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/9e6a938f-c9cb-4baf-b7d0-4316e45f874c">LeaveCriticalPolicySection</a>
 

 

