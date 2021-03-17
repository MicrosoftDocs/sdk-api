---
UID: NF:comsvcs.IComInstance2Events.OnObjectDestroy2
title: IComInstance2Events::OnObjectDestroy2 (comsvcs.h)
description: Generated when a client releases an object.
helpviewer_keywords: ["IComInstance2Events interface [COM+]","OnObjectDestroy2 method","IComInstance2Events.OnObjectDestroy2","IComInstance2Events::OnObjectDestroy2","OnObjectDestroy2","OnObjectDestroy2 method [COM+]","OnObjectDestroy2 method [COM+]","IComInstance2Events interface","_dtc_IComInstance2Events_OnObjectDestroy2","comsvcs/IComInstance2Events::OnObjectDestroy2","cos.icominstance2events_onobjectdestroy2"]
old-location: cos\icominstance2events_onobjectdestroy2.htm
tech.root: cos
ms.assetid: eeaf62b1-4c25-4232-829b-b2b147575ce9
ms.date: 12/05/2018
ms.keywords: IComInstance2Events interface [COM+],OnObjectDestroy2 method, IComInstance2Events.OnObjectDestroy2, IComInstance2Events::OnObjectDestroy2, OnObjectDestroy2, OnObjectDestroy2 method [COM+], OnObjectDestroy2 method [COM+],IComInstance2Events interface, _dtc_IComInstance2Events_OnObjectDestroy2, comsvcs/IComInstance2Events::OnObjectDestroy2, cos.icominstance2events_onobjectdestroy2
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
 - IComInstance2Events::OnObjectDestroy2
 - comsvcs/IComInstance2Events::OnObjectDestroy2
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
 - IComInstance2Events.OnObjectDestroy2
---

# IComInstance2Events::OnObjectDestroy2


## -description

Generated when a client releases an object.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The context identifier of the object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstance2events">IComInstance2Events</a>