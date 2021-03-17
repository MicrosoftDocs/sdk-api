---
UID: NF:comsvcs.IAppDomainHelper.DoCallback
title: IAppDomainHelper::DoCallback (comsvcs.h)
description: Switches into a given application domain (which the calling object must be bound to), executes the supplied callback function in that application domain, and then returns to the original application domain.
helpviewer_keywords: ["DoCallback","DoCallback method [COM+]","DoCallback method [COM+]","IAppDomainHelper interface","IAppDomainHelper interface [COM+]","DoCallback method","IAppDomainHelper.DoCallback","IAppDomainHelper::DoCallback","_cos_IAppDomainHelper_DoCallback","comsvcs/IAppDomainHelper::DoCallback","cos.iappdomainhelper_docallback"]
old-location: cos\iappdomainhelper_docallback.htm
tech.root: cos
ms.assetid: a82c2539-56cd-45ee-b673-a9440818bbc7
ms.date: 12/05/2018
ms.keywords: DoCallback, DoCallback method [COM+], DoCallback method [COM+],IAppDomainHelper interface, IAppDomainHelper interface [COM+],DoCallback method, IAppDomainHelper.DoCallback, IAppDomainHelper::DoCallback, _cos_IAppDomainHelper_DoCallback, comsvcs/IAppDomainHelper::DoCallback, cos.iappdomainhelper_docallback
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
 - IAppDomainHelper::DoCallback
 - comsvcs/IAppDomainHelper::DoCallback
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
 - IAppDomainHelper.DoCallback
---

# IAppDomainHelper::DoCallback


## -description

Switches into a given application domain (which the calling object must be bound to), executes the supplied callback function in that application domain, and then returns to the original application domain.

## -parameters

### -param pUnkAD [in]

Reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the application domain that you want to switch to. The object calling <b>DoCallback</b> must be bound to that application domain.

### -param __MIDL__IAppDomainHelper0001

Reference to the callback function. This function is executed in the application domain that you switched to. The parameter of this function, <i>pv</i>, comes from the <i>pPool</i> parameter, which is defined next.

### -param pPool [in]

This parameter is used to provide any data that the callback function might need.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iappdomainhelper">IAppDomainHelper</a>