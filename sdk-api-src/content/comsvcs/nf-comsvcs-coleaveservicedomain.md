---
UID: NF:comsvcs.CoLeaveServiceDomain
title: CoLeaveServiceDomain function (comsvcs.h)
description: Used to leave code that uses COM+ services.helpviewer_keywords: ["CoLeaveServiceDomain","CoLeaveServiceDomain function [COM+]","_cos_CoLeaveServiceDomain","comsvcs/CoLeaveServiceDomain","cos.coleaveservicedomain"]
old-location: cos\coleaveservicedomain.htm
tech.root: cossdk
ms.assetid: b67b3cf6-4462-4578-b61b-c5c61d809822
ms.date: 12/05/2018
ms.keywords: CoLeaveServiceDomain, CoLeaveServiceDomain function [COM+], _cos_CoLeaveServiceDomain, comsvcs/CoLeaveServiceDomain, cos.coleaveservicedomain
f1_keywords:
- comsvcs/CoLeaveServiceDomain
dev_langs:
- c++
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
- CoLeaveServiceDomain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoLeaveServiceDomain function


## -description


Used to leave code that uses COM+ services.


## -parameters




### -param pUnkStatus [in]

If you want to know the status of the transaction that is completed by the call, this must be a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactionstatus">ITransactionStatus</a> interface. If the enclosed code did not use transactions or if you do not need to know the transaction status, this parameter should be <b>NULL</b>. This parameter is ignored if it is non-<b>NULL</b> and if no transactions were used in the service domain.


## -remarks



Code that is enclosed between calls to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> runs in its own context and behaves as though it were a method that is called from an object created within the context.

<b>CoLeaveServiceDomain</b> triggers the server and then the client side policies as if a method call was returning. The current context is then popped from the context stack, and the context that was running when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> was called becomes the current context.

Because of their efficient design and because no thread marshaling is involved, using <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> involves significantly reduced overhead as compared to an equivalent method call.


<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> are particularly useful in applications, which can use these functions to access COM+ services without needing to create a component to do so.



The <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <b>CoLeaveServiceDomain</b> pairs can be nested. It is up to the user to make sure that the pairs of calls are balanced so that every call to <b>CoLeaveServiceDomain</b> matches a previous call to <b>CoEnterServiceDomain</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--services-without-components">COM+ Services Without Components</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>
 

 

