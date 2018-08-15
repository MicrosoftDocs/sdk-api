---
UID: NF:comsvcs.IAppDomainHelper.Initialize
title: IAppDomainHelper::Initialize
author: windows-sdk-content
description: Binds the calling object to the current application domain and provides a callback function for shutdown that is executed when the application domain is unloaded.
old-location: cos\iappdomainhelper_initialize.htm
old-project: cossdk
ms.assetid: c5cdff7f-6fb4-4f49-995a-63e4ecaef71a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAppDomainHelper interface [COM+],Initialize method, IAppDomainHelper.Initialize, IAppDomainHelper::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IAppDomainHelper interface, _cos_IAppDomainHelper_Initialize, comsvcs/IAppDomainHelper::Initialize, cos.iappdomainhelper_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IAppDomainHelper.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppDomainHelper::Initialize


## -description


Binds the calling object to the current application domain and provides a callback function for shutdown that is executed when the application domain is unloaded.


## -parameters




### -param pUnkAD [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the current application domain.


### -param __MIDL__IAppDomainHelper0000




### -param pPool [in]

This parameter is used to provide any data that the shutdown function might need.


#### - pfnCallbackCB [in]

Reference to the shutdown function that is executed when the application domain is unloaded. The parameter of this function, <i>pv</i>, comes from the <i>pPool</i> parameter, which is defined next.



#### pv


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2709f284-ca8c-404e-b568-b655f780549a">IAppDomainHelper</a>
 

 

