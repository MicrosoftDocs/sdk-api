---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolRecycleToTx
title: IComObjectPoolEvents::OnObjPoolRecycleToTx (comsvcs.h)
description: Generated when a transactional object is returned to the pool. (IComObjectPoolEvents.OnObjPoolRecycleToTx)
helpviewer_keywords: ["IComObjectPoolEvents interface [COM+]","OnObjPoolRecycleToTx method","IComObjectPoolEvents.OnObjPoolRecycleToTx","IComObjectPoolEvents::OnObjPoolRecycleToTx","OnObjPoolRecycleToTx","OnObjPoolRecycleToTx method [COM+]","OnObjPoolRecycleToTx method [COM+]","IComObjectPoolEvents interface","_dtc_icomobjectpoolevents_onobjpoolrecycletotx","comsvcs/IComObjectPoolEvents::OnObjPoolRecycleToTx","cos.icomobjectpoolevents_onobjpoolrecycletotx"]
old-location: cos\icomobjectpoolevents_onobjpoolrecycletotx.htm
tech.root: cos
ms.assetid: 6acae10b-9fda-4c73-b781-62a480271fd1
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolRecycleToTx method, IComObjectPoolEvents.OnObjPoolRecycleToTx, IComObjectPoolEvents::OnObjPoolRecycleToTx, OnObjPoolRecycleToTx, OnObjPoolRecycleToTx method [COM+], OnObjPoolRecycleToTx method [COM+],IComObjectPoolEvents interface, _dtc_icomobjectpoolevents_onobjpoolrecycletotx, comsvcs/IComObjectPoolEvents::OnObjPoolRecycleToTx, cos.icomobjectpoolevents_onobjpoolrecycletotx
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
 - IComObjectPoolEvents::OnObjPoolRecycleToTx
 - comsvcs/IComObjectPoolEvents::OnObjPoolRecycleToTx
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
 - IComObjectPoolEvents.OnObjPoolRecycleToTx
---

# IComObjectPoolEvents::OnObjPoolRecycleToTx


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

The GUID representing the transaction identifier.

### -param objid [in]

The unique identifier for this object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents">IComObjectPoolEvents</a>
