---
UID: NF:userenv.ProcessGroupPolicyCompletedEx
title: ProcessGroupPolicyCompletedEx function
author: windows-sdk-content
description: The ProcessGroupPolicyCompletedEx function notifies the system that the specified policy extension has finished applying policy. The function also reports the status of Resultant Set of Policy (RSoP) logging.
old-location: policy\processgrouppolicycompletedex.htm
tech.root: Policy
ms.assetid: 0d899190-7345-4762-ab59-b89e2e87d10f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ProcessGroupPolicyCompletedEx, ProcessGroupPolicyCompletedEx function [Group Policy], _win32_processgrouppolicycompletedex, policy.processgrouppolicycompletedex, userenv/ProcessGroupPolicyCompletedEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ProcessGroupPolicyCompletedEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ProcessGroupPolicyCompletedEx
: 
---

# ProcessGroupPolicyCompletedEx function


## -description


The 
    <b>ProcessGroupPolicyCompletedEx</b> function notifies the system that the specified policy extension has finished applying policy. The function also reports the status of Resultant Set of Policy (RSoP) logging.


## -parameters




### -param extensionId [in]

Specifies the unique <b>GUID</b> that identifies the policy extension.


### -param pAsyncHandle [in]

Asynchronous completion handle. This handle is passed to the 
<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a> callback function.


### -param dwStatus [in]

Specifies the completion status of asynchronous processing of policy.


### -param RsopStatus [in]

Specifies an <b>HRESULT</b> return code that indicates the status of RSoP logging.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>



<a href="https://msdn.microsoft.com/f88c8072-af4c-44e0-a816-ecb841dd1a78">ProcessGroupPolicyCompleted</a>



<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a>
 

 

