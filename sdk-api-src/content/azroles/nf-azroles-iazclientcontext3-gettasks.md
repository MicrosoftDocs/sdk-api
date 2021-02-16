---
UID: NF:azroles.IAzClientContext3.GetTasks
title: IAzClientContext3::GetTasks (azroles.h)
description: Returns a collection of the tasks, within the specified scope, that the principal represented by the current client context has permission to perform.
helpviewer_keywords: ["GetTasks","GetTasks method [Security]","GetTasks method [Security]","IAzClientContext3 interface","IAzClientContext3 interface [Security]","GetTasks method","IAzClientContext3.GetTasks","IAzClientContext3::GetTasks","azroles/IAzClientContext3::GetTasks","security.iazclientcontext3_gettasks_method"]
old-location: security\iazclientcontext3_gettasks_method.htm
tech.root: security
ms.assetid: 285f0e9a-8604-4475-8a73-ed33581f87f4
ms.date: 12/05/2018
ms.keywords: GetTasks, GetTasks method [Security], GetTasks method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],GetTasks method, IAzClientContext3.GetTasks, IAzClientContext3::GetTasks, azroles/IAzClientContext3::GetTasks, security.iazclientcontext3_gettasks_method
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzClientContext3::GetTasks
 - azroles/IAzClientContext3::GetTasks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.GetTasks
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.