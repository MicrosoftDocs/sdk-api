---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolGetFromTx
title: IComObjectPoolEvents::OnObjPoolGetFromTx (comsvcs.h)
description: Generated when a transactional object is obtained from the pool. (IComObjectPoolEvents.OnObjPoolGetFromTx)
helpviewer_keywords: ["IComObjectPoolEvents interface [COM+]","OnObjPoolGetFromTx method","IComObjectPoolEvents.OnObjPoolGetFromTx","IComObjectPoolEvents::OnObjPoolGetFromTx","OnObjPoolGetFromTx","OnObjPoolGetFromTx method [COM+]","OnObjPoolGetFromTx method [COM+]","IComObjectPoolEvents interface","_dtc_IComObjectPoolEvents_OnObjPoolGetFromTx","comsvcs/IComObjectPoolEvents::OnObjPoolGetFromTx","cos.icomobjectpoolevents_onobjpoolgetfromtx"]
old-location: cos\icomobjectpoolevents_onobjpoolgetfromtx.htm
tech.root: cos
ms.assetid: 977ab640-a9d5-47f5-ad47-ad2e1648fd6b
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolGetFromTx method, IComObjectPoolEvents.OnObjPoolGetFromTx, IComObjectPoolEvents::OnObjPoolGetFromTx, OnObjPoolGetFromTx, OnObjPoolGetFromTx method [COM+], OnObjPoolGetFromTx method [COM+],IComObjectPoolEvents interface, _dtc_IComObjectPoolEvents_OnObjPoolGetFromTx, comsvcs/IComObjectPoolEvents::OnObjPoolGetFromTx, cos.icomobjectpoolevents_onobjpoolgetfromtx
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
 - IComObjectPoolEvents::OnObjPoolGetFromTx
 - comsvcs/IComObjectPoolEvents::OnObjPoolGetFromTx
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
 - IComObjectPoolEvents.OnObjPoolGetFromTx
---

# IComObjectPoolEvents::OnObjPoolGetFromTx


## -description

Generated when a transactional object is obtained from the pool.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents">IComObjectPoolEvents</a>
