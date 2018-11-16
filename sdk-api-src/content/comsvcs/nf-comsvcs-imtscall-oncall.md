---
UID: NF:comsvcs.IMTSCall.OnCall
title: IMTSCall::OnCall
author: windows-sdk-content
description: Triggers the execution of the batch work implemented in this method.
old-location: cos\imtscall_oncall.htm
tech.root: cossdk
ms.assetid: 410ed66e-db55-41e6-8f09-df4fe3aad3f2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMTSCall interface [COM+],OnCall method, IMTSCall.OnCall, IMTSCall::OnCall, OnCall, OnCall method [COM+], OnCall method [COM+],IMTSCall interface, _cos_IMTSCall_OnCall, comsvcs/IMTSCall::OnCall, cos.imtscall_oncall
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMTSCall.OnCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IMTSCall.OnCall
: 
---

# IMTSCall::OnCall


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/en-us/library/ms687002(v=VS.85).aspx">IMTSCall</a> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/en-us/library/ms684294(v=VS.85).aspx">IServiceCall</a>.]

Triggers the execution of the batch work implemented in this method.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The batch work that is run in this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/en-us/library/ms679476(v=VS.85).aspx">MTSCreateActivity</a>. The batch work in this method is run using a call to either <a href="https://msdn.microsoft.com/en-us/library/ms681270(v=VS.85).aspx">IMTSActivity::SynchronousCall</a> or <a href="https://msdn.microsoft.com/en-us/library/ms686484(v=VS.85).aspx">IMTSActivity::AsyncCall</a>, using the <a href="https://msdn.microsoft.com/en-us/library/ms685105(v=VS.85).aspx">IMTSActivity</a> pointer that was returned from the call to <b>MTSCreateActivity</b>.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687002(v=VS.85).aspx">IMTSCall</a>
 

 

