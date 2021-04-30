---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolCreatePool
title: IComObjectPoolEvents2::OnObjPoolCreatePool (comsvcs.h)
description: Generated when a new pool is created.
helpviewer_keywords: ["IComObjectPoolEvents2 interface [COM+]","OnObjPoolCreatePool method","IComObjectPoolEvents2.OnObjPoolCreatePool","IComObjectPoolEvents2::OnObjPoolCreatePool","OnObjPoolCreatePool","OnObjPoolCreatePool method [COM+]","OnObjPoolCreatePool method [COM+]","IComObjectPoolEvents2 interface","_dtc_IComObjectPoolEvents2_OnObjPoolCreatePool","comsvcs/IComObjectPoolEvents2::OnObjPoolCreatePool","cos.icomobjectpoolevents2_onobjpoolcreatepool"]
old-location: cos\icomobjectpoolevents2_onobjpoolcreatepool.htm
tech.root: cos
ms.assetid: fa7a5ee4-8304-426c-9063-d25e2ed69668
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolCreatePool method, IComObjectPoolEvents2.OnObjPoolCreatePool, IComObjectPoolEvents2::OnObjPoolCreatePool, OnObjPoolCreatePool, OnObjPoolCreatePool method [COM+], OnObjPoolCreatePool method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolCreatePool, comsvcs/IComObjectPoolEvents2::OnObjPoolCreatePool, cos.icomobjectpoolevents2_onobjpoolcreatepool
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
 - IComObjectPoolEvents2::OnObjPoolCreatePool
 - comsvcs/IComObjectPoolEvents2::OnObjPoolCreatePool
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
 - IComObjectPoolEvents2.OnObjPoolCreatePool
---

# IComObjectPoolEvents2::OnObjPoolCreatePool


## -description

Generated when a new pool is created.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param dwMin [in]

The pool's minimum object value.

### -param dwMax [in]

The pool's maximum object value.

### -param dwTimeout [in]

The pool's time-out value.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents2">IComObjectPoolEvents2</a>