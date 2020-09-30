---
UID: NF:comsvcs.ISendMethodEvents.SendMethodCall
title: ISendMethodEvents::SendMethodCall (comsvcs.h)
description: Generated when a method is called through a component interface.
helpviewer_keywords: ["ISendMethodEvents interface [COM+]","SendMethodCall method","ISendMethodEvents.SendMethodCall","ISendMethodEvents::SendMethodCall","SendMethodCall","SendMethodCall method [COM+]","SendMethodCall method [COM+]","ISendMethodEvents interface","_cos_ISendMethodEvents_SendMethodCall","comsvcs/ISendMethodEvents::SendMethodCall","cos.isendmethodevents_sendmethodcall"]
old-location: cos\isendmethodevents_sendmethodcall.htm
tech.root: cos
ms.assetid: 730466c8-440c-42ee-899f-0d93007fbf8d
ms.date: 12/05/2018
ms.keywords: ISendMethodEvents interface [COM+],SendMethodCall method, ISendMethodEvents.SendMethodCall, ISendMethodEvents::SendMethodCall, SendMethodCall, SendMethodCall method [COM+], SendMethodCall method [COM+],ISendMethodEvents interface, _cos_ISendMethodEvents_SendMethodCall, comsvcs/ISendMethodEvents::SendMethodCall, cos.isendmethodevents_sendmethodcall
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
 - ISendMethodEvents::SendMethodCall
 - comsvcs/ISendMethodEvents::SendMethodCall
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
 - ISendMethodEvents.SendMethodCall
---

# ISendMethodEvents::SendMethodCall


## -description

Generated when a method is called through a component interface.

## -parameters

### -param pIdentity [in]

A pointer to the interface used to call the method.

### -param riid [in]

The ID of the interface used to call the method.

### -param dwMeth [in]

The method called.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isendmethodevents">ISendMethodEvents</a>