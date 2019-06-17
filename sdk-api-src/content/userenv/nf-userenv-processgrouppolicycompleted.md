---
UID: NF:userenv.ProcessGroupPolicyCompleted
title: ProcessGroupPolicyCompleted function (userenv.h)
author: windows-sdk-content
description: The ProcessGroupPolicyCompleted function notifies the system that the specified extension has finished applying policy.
old-location: policy\processgrouppolicycompleted.htm
tech.root: Policy
ms.assetid: f88c8072-af4c-44e0-a816-ecb841dd1a78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ProcessGroupPolicyCompleted, ProcessGroupPolicyCompleted function [Group Policy], _win32_processgrouppolicycompleted, policy.processgrouppolicycompleted, userenv/ProcessGroupPolicyCompleted
ms.topic: function
f1_keywords: ["userenv/ProcessGroupPolicyCompleted"]
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - ProcessGroupPolicyCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a> function.


### -param dwStatus [in]

Specifies the completion status of asynchronous processing.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nc-userenv-pfnprocessgrouppolicy">ProcessGroupPolicy</a>
 

 

