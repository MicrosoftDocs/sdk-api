---
UID: NF:userenv.ProcessGroupPolicyCompleted
title: ProcessGroupPolicyCompleted function
author: windows-sdk-content
description: The ProcessGroupPolicyCompleted function notifies the system that the specified extension has finished applying policy.
old-location: policy\processgrouppolicycompleted.htm
old-project: Policy
ms.assetid: f88c8072-af4c-44e0-a816-ecb841dd1a78
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ProcessGroupPolicyCompleted, ProcessGroupPolicyCompleted function [Group Policy], _win32_processgrouppolicycompleted, policy.processgrouppolicycompleted, userenv/ProcessGroupPolicyCompleted
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
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	ProcessGroupPolicyCompleted
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# ProcessGroupPolicyCompleted function


## -description


The 
    <b>ProcessGroupPolicyCompleted</b> function notifies the system that the specified extension has finished applying policy.


## -parameters




### -param extensionId [in]

Specifies the unique <b>GUID</b> that identifies the extension.


### -param pAsyncHandle [in]

Asynchronous completion handle. This handle is passed to the 
<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a> function.


### -param dwStatus [in]

Specifies the completion status of asynchronous processing.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>
 

 

