---
UID: NF:comsvcs.ISendMethodEvents.SendMethodReturn
title: ISendMethodEvents::SendMethodReturn (comsvcs.h)
description: Generated when a method called through a component interface returns control to the caller.
helpviewer_keywords: ["ISendMethodEvents interface [COM+]","SendMethodReturn method","ISendMethodEvents.SendMethodReturn","ISendMethodEvents::SendMethodReturn","SendMethodReturn","SendMethodReturn method [COM+]","SendMethodReturn method [COM+]","ISendMethodEvents interface","_cos_ISendMethodEvents_SendMethodReturn","comsvcs/ISendMethodEvents::SendMethodReturn","cos.isendmethodevents_sendmethodreturn"]
old-location: cos\isendmethodevents_sendmethodreturn.htm
tech.root: cos
ms.assetid: f9c8a680-644a-4617-866f-36e721bbc7aa
ms.date: 12/05/2018
ms.keywords: ISendMethodEvents interface [COM+],SendMethodReturn method, ISendMethodEvents.SendMethodReturn, ISendMethodEvents::SendMethodReturn, SendMethodReturn, SendMethodReturn method [COM+], SendMethodReturn method [COM+],ISendMethodEvents interface, _cos_ISendMethodEvents_SendMethodReturn, comsvcs/ISendMethodEvents::SendMethodReturn, cos.isendmethodevents_sendmethodreturn
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISendMethodEvents::SendMethodReturn
 - comsvcs/ISendMethodEvents::SendMethodReturn
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
 - ISendMethodEvents.SendMethodReturn
---

# ISendMethodEvents::SendMethodReturn


## -description

Generated when a method called through a component interface returns control to the caller.

## -parameters

### -param pIdentity [in]

A pointer to the interface used to call the method.

### -param riid [in]

The ID of the interface used to call the method.

### -param dwMeth [in]

The method called.

### -param hrCall [in]

The result returned by the method call.

### -param hrServer [in]

The result returned by the DCOM call to the server on which the component lives.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isendmethodevents">ISendMethodEvents</a>