---
UID: NF:userenv.LeaveCriticalPolicySection
title: LeaveCriticalPolicySection function
author: windows-sdk-content
description: The LeaveCriticalPolicySection function resumes the background application of policy. This function closes the handle to the policy section.
old-location: policy\leavecriticalpolicysection.htm
old-project: Policy
ms.assetid: 9e6a938f-c9cb-4baf-b7d0-4316e45f874c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: LeaveCriticalPolicySection, LeaveCriticalPolicySection function [Group Policy], _win32_leavecriticalpolicysection, policy.leavecriticalpolicysection, userenv/LeaveCriticalPolicySection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - LeaveCriticalPolicySection
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# LeaveCriticalPolicySection function


## -description


The 
    <b>LeaveCriticalPolicySection</b> function resumes the background application of policy. This function closes the handle to the policy section.


## -parameters




### -param hSection [in]

Handle to a policy section, which is returned by the 
<a href="https://msdn.microsoft.com/d17578b3-3a71-456b-97ca-961b81572528">EnterCriticalPolicySection</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d17578b3-3a71-456b-97ca-961b81572528">EnterCriticalPolicySection</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

