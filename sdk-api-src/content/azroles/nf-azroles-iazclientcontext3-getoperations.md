---
UID: NF:azroles.IAzClientContext3.GetOperations
title: IAzClientContext3::GetOperations
author: windows-sdk-content
description: Returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.
old-location: security\iazclientcontext3_getoperations_method.htm
old-project: SecAuthZ
ms.assetid: 0f5c7e2d-e88d-4236-888c-9bf5a425713c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetOperations, GetOperations method [Security], GetOperations method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],GetOperations method, IAzClientContext3.GetOperations, IAzClientContext3::GetOperations, azroles/IAzClientContext3::GetOperations, security.iazclientcontext3_getoperations_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.h
api_name:
-	IAzClientContext3.GetOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzClientContext3::GetOperations


## -description


The <b>GetOperations</b> method returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.


## -parameters




### -param bstrScopeName [in]

The name of the scope to check.


### -param ppOperationCollection [out]

The address of a pointer to the collection of operations that the principal represented by the current client context has permission to perform.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



