---
UID: NF:comsvcs.IComMethodEvents.OnMethodCall
title: IComMethodEvents::OnMethodCall (comsvcs.h)
description: Generated when an object's method is called. (IComMethodEvents.OnMethodCall)
helpviewer_keywords: ["IComMethodEvents interface [COM+]","OnMethodCall method","IComMethodEvents.OnMethodCall","IComMethodEvents::OnMethodCall","OnMethodCall","OnMethodCall method [COM+]","OnMethodCall method [COM+]","IComMethodEvents interface","_dtc_IComMethodEvents_OnMethodCall","comsvcs/IComMethodEvents::OnMethodCall","cos.icommethodevents_onmethodcall"]
old-location: cos\icommethodevents_onmethodcall.htm
tech.root: cos
ms.assetid: 5d68fe2c-7032-46d2-b88d-0b4f81c74760
ms.date: 12/05/2018
ms.keywords: IComMethodEvents interface [COM+],OnMethodCall method, IComMethodEvents.OnMethodCall, IComMethodEvents::OnMethodCall, OnMethodCall, OnMethodCall method [COM+], OnMethodCall method [COM+],IComMethodEvents interface, _dtc_IComMethodEvents_OnMethodCall, comsvcs/IComMethodEvents::OnMethodCall, cos.icommethodevents_onmethodcall
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
 - IComMethodEvents::OnMethodCall
 - comsvcs/IComMethodEvents::OnMethodCall
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
 - IComMethodEvents.OnMethodCall
---

# IComMethodEvents::OnMethodCall


## -description

Generated when an object's method is called.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param oid [in]

The just-in-time (JIT) activated object.

### -param guidCid [in]

The CLSID for the object being called.

### -param guidRid [in]

The identifier of the method being called.

### -param iMeth [in]

The v-table index of the method.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a>
