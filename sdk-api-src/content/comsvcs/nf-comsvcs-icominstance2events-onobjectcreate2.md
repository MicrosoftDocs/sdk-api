---
UID: NF:comsvcs.IComInstance2Events.OnObjectCreate2
title: IComInstance2Events::OnObjectCreate2 (comsvcs.h)
description: Generated when a client creates an object.
helpviewer_keywords: ["IComInstance2Events interface [COM+]","OnObjectCreate2 method","IComInstance2Events.OnObjectCreate2","IComInstance2Events::OnObjectCreate2","OnObjectCreate2","OnObjectCreate2 method [COM+]","OnObjectCreate2 method [COM+]","IComInstance2Events interface","_dtc_IComInstance2Events_OnObjectCreate2","comsvcs/IComInstance2Events::OnObjectCreate2","cos.icominstance2events_onobjectcreate2"]
old-location: cos\icominstance2events_onobjectcreate2.htm
tech.root: cos
ms.assetid: b7c359b8-2d49-4982-836b-50d749758fa6
ms.date: 12/05/2018
ms.keywords: IComInstance2Events interface [COM+],OnObjectCreate2 method, IComInstance2Events.OnObjectCreate2, IComInstance2Events::OnObjectCreate2, OnObjectCreate2, OnObjectCreate2 method [COM+], OnObjectCreate2 method [COM+],IComInstance2Events interface, _dtc_IComInstance2Events_OnObjectCreate2, comsvcs/IComInstance2Events::OnObjectCreate2, cos.icominstance2events_onobjectcreate2
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
 - IComInstance2Events::OnObjectCreate2
 - comsvcs/IComInstance2Events::OnObjectCreate2
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
 - IComInstance2Events.OnObjectCreate2
---

# IComInstance2Events::OnObjectCreate2


## -description

Generated when a client creates an object.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidActivity [in]

The identifier of the activity in which the object is created.

### -param clsid [in]

The CLSID of the object being created.

### -param tsid [in]

The transaction stream identifier, which is unique for correlation to objects.

### -param CtxtID [in]

The context identifier for this object.

### -param ObjectID [in]

The initial JIT-activated object.

### -param guidPartition [in]

The partition identifier for which this instance is created.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstance2events">IComInstance2Events</a>