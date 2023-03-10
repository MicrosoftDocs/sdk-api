---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolRecycleToTx2
title: IComObjectPool2Events::OnObjPoolRecycleToTx2 (comsvcs.h)
description: Generated when a transactional object is returned to the pool. (IComObjectPool2Events.OnObjPoolRecycleToTx2)
helpviewer_keywords: ["IComObjectPool2Events interface [COM+]","OnObjPoolRecycleToTx2 method","IComObjectPool2Events.OnObjPoolRecycleToTx2","IComObjectPool2Events::OnObjPoolRecycleToTx2","OnObjPoolRecycleToTx2","OnObjPoolRecycleToTx2 method [COM+]","OnObjPoolRecycleToTx2 method [COM+]","IComObjectPool2Events interface","_dtc_IComObjectPool2Events_OnObjPoolRecycleToTx2","comsvcs/IComObjectPool2Events::OnObjPoolRecycleToTx2","cos.icomobjectpool2events_onobjpoolrecycletotx2"]
old-location: cos\icomobjectpool2events_onobjpoolrecycletotx2.htm
tech.root: cos
ms.assetid: f737289f-c990-455e-bc9b-e94f25c9297f
ms.date: 12/05/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolRecycleToTx2 method, IComObjectPool2Events.OnObjPoolRecycleToTx2, IComObjectPool2Events::OnObjPoolRecycleToTx2, OnObjPoolRecycleToTx2, OnObjPoolRecycleToTx2 method [COM+], OnObjPoolRecycleToTx2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolRecycleToTx2, comsvcs/IComObjectPool2Events::OnObjPoolRecycleToTx2, cos.icomobjectpool2events_onobjpoolrecycletotx2
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
 - IComObjectPool2Events::OnObjPoolRecycleToTx2
 - comsvcs/IComObjectPool2Events::OnObjPoolRecycleToTx2
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
 - IComObjectPool2Events.OnObjPoolRecycleToTx2
---

# IComObjectPool2Events::OnObjPoolRecycleToTx2


## -description

Generated when a transactional object is returned to the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidActivity [in]

The activity ID for which the object is created.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param guidTx [in]

The transaction identifier.

### -param objid [in]

The unique identifier for this object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpool2events">IComObjectPool2Events</a>
