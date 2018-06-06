---
UID: NF:comsvcs.IMTSCall.OnCall
title: IMTSCall::OnCall
author: windows-sdk-content
description: Triggers the execution of the batch work implemented in this method.
old-location: cos\imtscall_oncall.htm
old-project: cossdk
ms.assetid: 410ed66e-db55-41e6-8f09-df4fe3aad3f2
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMTSCall interface [COM+],OnCall method, IMTSCall.OnCall, IMTSCall::OnCall, OnCall, OnCall method [COM+], OnCall method [COM+],IMTSCall interface, _cos_IMTSCall_OnCall, comsvcs/IMTSCall::OnCall, cos.imtscall_oncall
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMTSCall.OnCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMTSCall::OnCall


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>.]

Triggers the execution of the batch work implemented in this method.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The batch work that is run in this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a>. The batch work in this method is run using a call to either <a href="https://msdn.microsoft.com/4f69956b-fdb3-47c4-9a19-e9f39a8d5e06">IMTSActivity::SynchronousCall</a> or <a href="https://msdn.microsoft.com/ccbb96e8-9fb8-40b4-b027-432ba8c400c7">IMTSActivity::AsyncCall</a>, using the <a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a> pointer that was returned from the call to <b>MTSCreateActivity</b>.





## -see-also




<a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a>
 

 

