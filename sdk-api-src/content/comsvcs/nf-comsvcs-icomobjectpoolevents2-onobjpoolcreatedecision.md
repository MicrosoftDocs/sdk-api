---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolCreateDecision
title: IComObjectPoolEvents2::OnObjPoolCreateDecision (comsvcs.h)
description: Generated when a pool provides a requesting client with an existing object or creates a new one.
helpviewer_keywords: ["IComObjectPoolEvents2 interface [COM+]","OnObjPoolCreateDecision method","IComObjectPoolEvents2.OnObjPoolCreateDecision","IComObjectPoolEvents2::OnObjPoolCreateDecision","OnObjPoolCreateDecision","OnObjPoolCreateDecision method [COM+]","OnObjPoolCreateDecision method [COM+]","IComObjectPoolEvents2 interface","_dtc_IComObjectPoolEvents2_OnObjPoolCreateDecision","comsvcs/IComObjectPoolEvents2::OnObjPoolCreateDecision","cos.icomobjectpoolevents2_onobjpoolcreatedecision"]
old-location: cos\icomobjectpoolevents2_onobjpoolcreatedecision.htm
tech.root: cos
ms.assetid: a66c00ac-b9b9-431e-b1c8-6642cb35ec3c
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolCreateDecision method, IComObjectPoolEvents2.OnObjPoolCreateDecision, IComObjectPoolEvents2::OnObjPoolCreateDecision, OnObjPoolCreateDecision, OnObjPoolCreateDecision method [COM+], OnObjPoolCreateDecision method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolCreateDecision, comsvcs/IComObjectPoolEvents2::OnObjPoolCreateDecision, cos.icomobjectpoolevents2_onobjpoolcreatedecision
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
 - IComObjectPoolEvents2::OnObjPoolCreateDecision
 - comsvcs/IComObjectPoolEvents2::OnObjPoolCreateDecision
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
 - IComObjectPoolEvents2.OnObjPoolCreateDecision
---

# IComObjectPoolEvents2::OnObjPoolCreateDecision


## -description

Generated when a pool provides a requesting client with an existing object or creates a new one.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param dwThreadsWaiting [in]

The number of threads waiting for an object.

### -param dwAvail [in]

The number of free objects in the pool.

### -param dwCreated [in]

The number of total objects in the pool.

### -param dwMin [in]

The pool's minimum object value.

### -param dwMax [in]

The pool's maximum object value.

## -returns

The user verifies the return values from this method.

## -remarks

When a component is configured for object pooling, the pool is populated with objects up to the specified minimum level. As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool. If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents2">IComObjectPoolEvents2</a>