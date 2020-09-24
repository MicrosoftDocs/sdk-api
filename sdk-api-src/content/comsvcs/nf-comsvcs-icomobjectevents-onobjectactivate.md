---
UID: NF:comsvcs.IComObjectEvents.OnObjectActivate
title: IComObjectEvents::OnObjectActivate (comsvcs.h)
description: Generated when an object gets an instance of a new JIT-activated object.
helpviewer_keywords: ["IComObjectEvents interface [COM+]","OnObjectActivate method","IComObjectEvents.OnObjectActivate","IComObjectEvents::OnObjectActivate","OnObjectActivate","OnObjectActivate method [COM+]","OnObjectActivate method [COM+]","IComObjectEvents interface","_dtc_IComObjectEvents_OnObjectActivate","comsvcs/IComObjectEvents::OnObjectActivate","cos.icomobjectevents_onobjectactivate"]
old-location: cos\icomobjectevents_onobjectactivate.htm
tech.root: cos
ms.assetid: 149e3820-0d5b-46ee-9be9-22850115a7c7
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnObjectActivate method, IComObjectEvents.OnObjectActivate, IComObjectEvents::OnObjectActivate, OnObjectActivate, OnObjectActivate method [COM+], OnObjectActivate method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnObjectActivate, comsvcs/IComObjectEvents::OnObjectActivate, cos.icomobjectevents_onobjectactivate
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
 - IComObjectEvents::OnObjectActivate
 - comsvcs/IComObjectEvents::OnObjectActivate
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
 - IComObjectEvents.OnObjectActivate
---

# IComObjectEvents::OnObjectActivate


## -description

Generated when an object gets an instance of a new JIT-activated object.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The GUID of the current context.

### -param ObjectID [in]

The JIT-activated object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>