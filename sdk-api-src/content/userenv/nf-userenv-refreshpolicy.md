---
UID: NF:userenv.RefreshPolicy
title: RefreshPolicy function
author: windows-sdk-content
description: The RefreshPolicy function causes policy to be applied immediately on the client computer.
old-location: policy\refreshpolicy.htm
old-project: Policy
ms.assetid: e08cb006-d174-4506-87f0-580660bd4023
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RefreshPolicy, RefreshPolicy function [Group Policy], _win32_refreshpolicy, policy.refreshpolicy, userenv/RefreshPolicy
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	RefreshPolicy
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# RefreshPolicy function


## -description


The
    <b>RefreshPolicy</b> function causes policy to be applied immediately on the client computer. To apply policy and specify the type of refresh that should occur, you can call the extended function 
<a href="https://msdn.microsoft.com/905ab96b-a7f2-4bb4-a539-385f78284644">RefreshPolicyEx</a>.


## -parameters




### -param bMachine [in]

Specifies whether to refresh the computer policy or user policy. If this value is <b>TRUE</b>, the system refreshes the computer policy. If this value is <b>FALSE</b>, the system refreshes the user policy.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



By default, policy is reapplied every 90 minutes.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>
 

 

