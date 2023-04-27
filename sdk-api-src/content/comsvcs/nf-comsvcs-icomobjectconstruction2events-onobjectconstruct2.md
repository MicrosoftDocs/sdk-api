---
UID: NF:comsvcs.IComObjectConstruction2Events.OnObjectConstruct2
title: IComObjectConstruction2Events::OnObjectConstruct2 (comsvcs.h)
description: Generated when a constructed object is created. (IComObjectConstruction2Events.OnObjectConstruct2)
helpviewer_keywords: ["IComObjectConstruction2Events interface [COM+]","OnObjectConstruct2 method","IComObjectConstruction2Events.OnObjectConstruct2","IComObjectConstruction2Events::OnObjectConstruct2","OnObjectConstruct2","OnObjectConstruct2 method [COM+]","OnObjectConstruct2 method [COM+]","IComObjectConstruction2Events interface","_dtc_IComObjectConstruction2Events_OnObjectConstruct2","comsvcs/IComObjectConstruction2Events::OnObjectConstruct2","cos.icomobjectconstruction2events_onobjectconstruct2"]
old-location: cos\icomobjectconstruction2events_onobjectconstruct2.htm
tech.root: cos
ms.assetid: c71157b3-e5e4-4b20-bab7-7047587a20f1
ms.date: 12/05/2018
ms.keywords: IComObjectConstruction2Events interface [COM+],OnObjectConstruct2 method, IComObjectConstruction2Events.OnObjectConstruct2, IComObjectConstruction2Events::OnObjectConstruct2, OnObjectConstruct2, OnObjectConstruct2 method [COM+], OnObjectConstruct2 method [COM+],IComObjectConstruction2Events interface, _dtc_IComObjectConstruction2Events_OnObjectConstruct2, comsvcs/IComObjectConstruction2Events::OnObjectConstruct2, cos.icomobjectconstruction2events_onobjectconstruct2
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
 - IComObjectConstruction2Events::OnObjectConstruct2
 - comsvcs/IComObjectConstruction2Events::OnObjectConstruct2
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
 - IComObjectConstruction2Events.OnObjectConstruct2
---

# IComObjectConstruction2Events::OnObjectConstruct2


## -description

Generated when a constructed object is created.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param sConstructString [in]

The object construction string.

### -param oid [in]

The unique constructed object identifier.

### -param guidPartition [in]

The partition identifier for which this instance is created.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectconstruction2events">IComObjectConstruction2Events</a>
