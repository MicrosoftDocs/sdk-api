---
UID: NF:comsvcs.IComObjectConstructionEvents.OnObjectConstruct
title: IComObjectConstructionEvents::OnObjectConstruct (comsvcs.h)
description: Generated when a constructed object is created. (IComObjectConstructionEvents.OnObjectConstruct)
helpviewer_keywords: ["IComObjectConstructionEvents interface [COM+]","OnObjectConstruct method","IComObjectConstructionEvents.OnObjectConstruct","IComObjectConstructionEvents::OnObjectConstruct","OnObjectConstruct","OnObjectConstruct method [COM+]","OnObjectConstruct method [COM+]","IComObjectConstructionEvents interface","_dtc_IComObjectConstructionEvents_OnObjectConstruct","comsvcs/IComObjectConstructionEvents::OnObjectConstruct","cos.icomobjectconstructionevents_onobjectconstruct"]
old-location: cos\icomobjectconstructionevents_onobjectconstruct.htm
tech.root: cos
ms.assetid: 8a90e561-79a0-4490-bbc8-f376e4278ab9
ms.date: 12/05/2018
ms.keywords: IComObjectConstructionEvents interface [COM+],OnObjectConstruct method, IComObjectConstructionEvents.OnObjectConstruct, IComObjectConstructionEvents::OnObjectConstruct, OnObjectConstruct, OnObjectConstruct method [COM+], OnObjectConstruct method [COM+],IComObjectConstructionEvents interface, _dtc_IComObjectConstructionEvents_OnObjectConstruct, comsvcs/IComObjectConstructionEvents::OnObjectConstruct, cos.icomobjectconstructionevents_onobjectconstruct
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
 - IComObjectConstructionEvents::OnObjectConstruct
 - comsvcs/IComObjectConstructionEvents::OnObjectConstruct
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
 - IComObjectConstructionEvents.OnObjectConstruct
---

# IComObjectConstructionEvents::OnObjectConstruct


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

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectconstructionevents">IComObjectConstructionEvents</a>
