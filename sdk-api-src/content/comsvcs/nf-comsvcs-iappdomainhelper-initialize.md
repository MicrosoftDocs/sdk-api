---
UID: NF:comsvcs.IAppDomainHelper.Initialize
title: IAppDomainHelper::Initialize (comsvcs.h)
description: Binds the calling object to the current application domain and provides a callback function for shutdown that is executed when the application domain is unloaded.
helpviewer_keywords: ["IAppDomainHelper interface [COM+]","Initialize method","IAppDomainHelper.Initialize","IAppDomainHelper::Initialize","Initialize","Initialize method [COM+]","Initialize method [COM+]","IAppDomainHelper interface","_cos_IAppDomainHelper_Initialize","comsvcs/IAppDomainHelper::Initialize","cos.iappdomainhelper_initialize"]
old-location: cos\iappdomainhelper_initialize.htm
tech.root: cos
ms.assetid: c5cdff7f-6fb4-4f49-995a-63e4ecaef71a
ms.date: 12/05/2018
ms.keywords: IAppDomainHelper interface [COM+],Initialize method, IAppDomainHelper.Initialize, IAppDomainHelper::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IAppDomainHelper interface, _cos_IAppDomainHelper_Initialize, comsvcs/IAppDomainHelper::Initialize, cos.iappdomainhelper_initialize
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppDomainHelper::Initialize
 - comsvcs/IAppDomainHelper::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IAppDomainHelper.Initialize
---

# IAppDomainHelper::Initialize


## -description

Binds the calling object to the current application domain and provides a callback function for shutdown that is executed when the application domain is unloaded.

## -parameters

### -param pUnkAD [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the current application domain.

### -param __MIDL__IAppDomainHelper0000

Reference to the shutdown function that is executed when the application domain is unloaded. The parameter of this function, <i>pv</i>, comes from the <i>pPool</i> parameter, which is defined next.

### -param pPool [in]

This parameter is used to provide any data that the shutdown function might need.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iappdomainhelper">IAppDomainHelper</a>