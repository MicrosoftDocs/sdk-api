---
UID: NF:azroles.IAzClientContext3.GetTasks
title: IAzClientContext3::GetTasks
author: windows-sdk-content
description: Returns a collection of the tasks, within the specified scope, that the principal represented by the current client context has permission to perform.
old-location: security\iazclientcontext3_gettasks_method.htm
old-project: secauthz
ms.assetid: 285f0e9a-8604-4475-8a73-ed33581f87f4
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetTasks, GetTasks method [Security], GetTasks method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],GetTasks method, IAzClientContext3.GetTasks, IAzClientContext3::GetTasks, azroles/IAzClientContext3::GetTasks, security.iazclientcontext3_gettasks_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.GetTasks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzClientContext3::GetTasks


## -description


The <b>GetTasks</b> method returns a collection of the tasks, within the specified scope, that the principal represented by the current client context has permission to perform.


## -parameters




### -param bstrScopeName [in]

The name of the scope to check.


### -param ppTaskCollection [out]

The address of a pointer to the collection of tasks that the principal represented by the current client context has permission to perform.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



