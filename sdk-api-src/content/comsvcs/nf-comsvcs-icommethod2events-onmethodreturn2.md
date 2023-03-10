---
UID: NF:comsvcs.IComMethod2Events.OnMethodReturn2
title: IComMethod2Events::OnMethodReturn2 (comsvcs.h)
description: Generated when an object's method returns. (IComMethod2Events.OnMethodReturn2)
helpviewer_keywords: ["IComMethod2Events interface [COM+]","OnMethodReturn2 method","IComMethod2Events.OnMethodReturn2","IComMethod2Events::OnMethodReturn2","OnMethodReturn2","OnMethodReturn2 method [COM+]","OnMethodReturn2 method [COM+]","IComMethod2Events interface","_dtc_IComMethod2Events_OnMethodReturn2","comsvcs/IComMethod2Events::OnMethodReturn2","cos.icommethod2events_onmethodreturn2"]
old-location: cos\icommethod2events_onmethodreturn2.htm
tech.root: cos
ms.assetid: cf5a7b69-a794-4497-99c9-20c41d454753
ms.date: 12/05/2018
ms.keywords: IComMethod2Events interface [COM+],OnMethodReturn2 method, IComMethod2Events.OnMethodReturn2, IComMethod2Events::OnMethodReturn2, OnMethodReturn2, OnMethodReturn2 method [COM+], OnMethodReturn2 method [COM+],IComMethod2Events interface, _dtc_IComMethod2Events_OnMethodReturn2, comsvcs/IComMethod2Events::OnMethodReturn2, cos.icommethod2events_onmethodreturn2
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
 - IComMethod2Events::OnMethodReturn2
 - comsvcs/IComMethod2Events::OnMethodReturn2
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
 - IComMethod2Events.OnMethodReturn2
---

# IComMethod2Events::OnMethodReturn2


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

The identifier of the method being called.

### -param dwThread [in]

The identifier of the thread executing the call.

### -param iMeth [in]

The v-table index of the method.

### -param hresult [in]

The result of the method call.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethod2events">IComMethod2Events</a>
