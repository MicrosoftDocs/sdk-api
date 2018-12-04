---
UID: NF:comsvcs.MTSCreateActivity
title: MTSCreateActivity function
author: windows-sdk-content
description: Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.
old-location: cos\mtscreateactivity.htm
tech.root: cossdk
ms.assetid: 25ae1f2e-f937-4d06-9709-ded2fc8c5777
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: MTSCreateActivity, MTSCreateActivity function [COM+], _cos_MTSCreateActivity, comsvcs/MTSCreateActivity, cos.mtscreateactivity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - MTSCreateActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MTSCreateActivity function


## -description


<p class="CCE_Message">[<b>MTSCreateActivity</b> is available for in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> function.]

Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.


## -parameters




### -param riid [in]

The ID of the interface to be returned by the <i>ppObj</i> parameter. This parameter should always be IID_IMTSActivity so that a pointer to <a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a> is returned.


### -param ppobj [out]

A pointer to the interface of an activity object. The activity object is automatically created by the call to <b>MTSCreateActivity</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



<b>MTSCreateActivity</b> creates an activity object that is used to submit batch work to the COM+ system. The batch work that is submitted through <b>MTSCreateActivity</b> can be either synchronous or asynchronous and runs in a single-threaded apartment (STA).

<b>MTSCreateActivity</b> returns a pointer to the <a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a> interface of the object that is created by the call to <b>MTSCreateActivity</b>. By using the methods of <b>IMTSActivity</b>, you determine whether the batch work is done synchronously or asynchronously. The batch work itself is implemented through the <a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a> interface.





## -see-also




<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>
 

 

