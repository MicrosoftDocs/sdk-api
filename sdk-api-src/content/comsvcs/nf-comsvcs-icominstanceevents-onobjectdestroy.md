---
UID: NF:comsvcs.IComInstanceEvents.OnObjectDestroy
title: IComInstanceEvents::OnObjectDestroy (comsvcs.h)
description: Generated when an object is released by a client.
helpviewer_keywords: ["IComInstanceEvents interface [COM+]","OnObjectDestroy method","IComInstanceEvents.OnObjectDestroy","IComInstanceEvents::OnObjectDestroy","OnObjectDestroy","OnObjectDestroy method [COM+]","OnObjectDestroy method [COM+]","IComInstanceEvents interface","_dtc_IComInstanceEvents_OnObjectDestroy","comsvcs/IComInstanceEvents::OnObjectDestroy","cos.icominstanceevents_onobjectdestroy"]
old-location: cos\icominstanceevents_onobjectdestroy.htm
tech.root: cos
ms.assetid: 3eea4171-a177-4adc-bd9a-856a558ba3d8
ms.date: 12/05/2018
ms.keywords: IComInstanceEvents interface [COM+],OnObjectDestroy method, IComInstanceEvents.OnObjectDestroy, IComInstanceEvents::OnObjectDestroy, OnObjectDestroy, OnObjectDestroy method [COM+], OnObjectDestroy method [COM+],IComInstanceEvents interface, _dtc_IComInstanceEvents_OnObjectDestroy, comsvcs/IComInstanceEvents::OnObjectDestroy, cos.icominstanceevents_onobjectdestroy
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
 - IComInstanceEvents::OnObjectDestroy
 - comsvcs/IComInstanceEvents::OnObjectDestroy
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
 - IComInstanceEvents.OnObjectDestroy
---

# IComInstanceEvents::OnObjectDestroy


## -description

Generated when an object is released by a client.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The context identifier of the object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstanceevents">IComInstanceEvents</a>