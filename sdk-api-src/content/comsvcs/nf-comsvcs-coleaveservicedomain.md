---
UID: NF:comsvcs.CoLeaveServiceDomain
title: CoLeaveServiceDomain function
author: windows-sdk-content
description: Used to leave code that uses COM+ services.
old-location: cos\coleaveservicedomain.htm
old-project: cossdk
ms.assetid: b67b3cf6-4462-4578-b61b-c5c61d809822
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: CoLeaveServiceDomain, CoLeaveServiceDomain function [COM+], _cos_CoLeaveServiceDomain, comsvcs/CoLeaveServiceDomain, cos.coleaveservicedomain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - CoLeaveServiceDomain
product: Windows
targetos: Windows
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
---

# CoLeaveServiceDomain function


## -description


Used to leave code that uses COM+ services.


## -parameters




### -param pUnkStatus [in]

If you want to know the status of the transaction that is completed by the call, this must be a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of an object that implements the <a href="https://msdn.microsoft.com/df5eba93-6db7-478c-b6d7-831c20398d66">ITransactionStatus</a> interface. If the enclosed code did not use transactions or if you do not need to know the transaction status, this parameter should be <b>NULL</b>. This parameter is ignored if it is non-<b>NULL</b> and if no transactions were used in the service domain.


## -returns



This function does not return a value.




## -remarks



Code that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> runs in its own context and behaves as though it were a method that is called from an object created within the context.

<b>CoLeaveServiceDomain</b> triggers the server and then the client side policies as if a method call was returning. The current context is then popped from the context stack, and the context that was running when <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> was called becomes the current context.

Because of their efficient design and because no thread marshaling is involved, using <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> involves significantly reduced overhead as compared to an equivalent method call.


<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> are particularly useful in applications, which can use these functions to access COM+ services without needing to create a component to do so.



The <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> pairs can be nested. It is up to the user to make sure that the pairs of calls are balanced so that every call to <b>CoLeaveServiceDomain</b> matches a previous call to <b>CoEnterServiceDomain</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ef67411-334b-476e-b9b7-3677b24ab7df">COM+ Services Without Components</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>
 

 

