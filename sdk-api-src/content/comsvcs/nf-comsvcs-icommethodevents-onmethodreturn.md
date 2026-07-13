---
UID: NF:comsvcs.IComMethodEvents.OnMethodReturn
title: IComMethodEvents::OnMethodReturn (comsvcs.h)
description: Generated when an object's method returns. (IComMethodEvents.OnMethodReturn)
helpviewer_keywords: ["IComMethodEvents interface [COM+]","OnMethodReturn method","IComMethodEvents.OnMethodReturn","IComMethodEvents::OnMethodReturn","OnMethodReturn","OnMethodReturn method [COM+]","OnMethodReturn method [COM+]","IComMethodEvents interface","_dtc_icommethodevents_onmethodreturn","comsvcs/IComMethodEvents::OnMethodReturn","cos.icommethodevents_onmethodreturn"]
old-location: cos\icommethodevents_onmethodreturn.htm
tech.root: cos
ms.assetid: ade20bfc-0b50-4663-a1d3-14e2bd0c19a1
ms.date: 12/05/2018
ms.keywords: IComMethodEvents interface [COM+],OnMethodReturn method, IComMethodEvents.OnMethodReturn, IComMethodEvents::OnMethodReturn, OnMethodReturn, OnMethodReturn method [COM+], OnMethodReturn method [COM+],IComMethodEvents interface, _dtc_icommethodevents_onmethodreturn, comsvcs/IComMethodEvents::OnMethodReturn, cos.icommethodevents_onmethodreturn
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
 - IComMethodEvents::OnMethodReturn
 - comsvcs/IComMethodEvents::OnMethodReturn
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
 - IComMethodEvents.OnMethodReturn
---

# IComMethodEvents::OnMethodReturn


## -description

Generated when an object's method returns.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param oid [in]

The just-in-time (JIT) activated object.

### -param guidCid [in]

The CLSID for the object being called.

### -param guidRid [in]

The identifier of the method.

### -param iMeth [in]

The v-table index of the method.

### -param hresult [in]

The result of the method call.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a>
