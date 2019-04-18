---
UID: NF:comsvcs.IMTSActivity.AsyncCall
title: IMTSActivity::AsyncCall (comsvcs.h)
author: windows-sdk-content
description: Performs the user-defined work asynchronously.
old-location: cos\imtsactivity_asynccall.htm
tech.root: cossdk
ms.assetid: ccbb96e8-9fb8-40b4-b027-432ba8c400c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AsyncCall, AsyncCall method [COM+], AsyncCall method [COM+],IMTSActivity interface, IMTSActivity interface [COM+],AsyncCall method, IMTSActivity.AsyncCall, IMTSActivity::AsyncCall, _cos_IMTSActivity_AsyncCall, comsvcs/IMTSActivity::AsyncCall, cos.imtsactivity_asynccall
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMTSActivity.AsyncCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMTSActivity::AsyncCall


## -description


Performs the user-defined work asynchronously.


## -parameters




### -param pCall [in]

A pointer to the <a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a> interface that is used to implement the batch work.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The batch work that is run using this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a>.


A return value of S_OK indicates that the batch work was accepted by the activity to run asynchronously. However, it does not necessarily mean that the batch work successfully completed.




## -see-also




<a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a>
 

 

