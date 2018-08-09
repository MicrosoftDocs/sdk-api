---
UID: NF:comsvcs.IMTSActivity.UnbindFromThread
title: IMTSActivity::UnbindFromThread
author: windows-sdk-content
description: Unbinds the batch work that is submitted using IMTSActivity::AsyncCall or IMTSActivity::SynchronousCall from the thread on which it is running.
old-location: cos\imtsactivity_unbindfromthread.htm
old-project: cossdk
ms.assetid: cb4c4f63-2a6e-4df7-8886-19d45e28d81a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMTSActivity interface [COM+],UnbindFromThread method, IMTSActivity.UnbindFromThread, IMTSActivity::UnbindFromThread, UnbindFromThread, UnbindFromThread method [COM+], UnbindFromThread method [COM+],IMTSActivity interface, _cos_IMTSActivity_UnbindFromThread, comsvcs/IMTSActivity::UnbindFromThread, cos.imtsactivity_unbindfromthread
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
 - IMTSActivity.UnbindFromThread
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMTSActivity::UnbindFromThread


## -description


Unbinds the batch work that is submitted using <a href="https://msdn.microsoft.com/ccbb96e8-9fb8-40b4-b027-432ba8c400c7">IMTSActivity::AsyncCall</a> or <a href="https://msdn.microsoft.com/4f69956b-fdb3-47c4-9a19-e9f39a8d5e06">IMTSActivity::SynchronousCall</a> from the thread on which it is running. It has no effect if the batch work was not previously bound to a thread.

This method is designed to be called from the implementation of the <a href="https://msdn.microsoft.com/410ed66e-db55-41e6-8f09-df4fe3aad3f2">IMTSCall::OnCall</a> method.



## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a>
 

 

