---
UID: NF:comsvcs.IComInstanceEvents.OnObjectCreate
title: IComInstanceEvents::OnObjectCreate (comsvcs.h)
description: Generated when an object is created by a client.
helpviewer_keywords: ["IComInstanceEvents interface [COM+]","OnObjectCreate method","IComInstanceEvents.OnObjectCreate","IComInstanceEvents::OnObjectCreate","OnObjectCreate","OnObjectCreate method [COM+]","OnObjectCreate method [COM+]","IComInstanceEvents interface","_dtc_icominstanceevents_onobjectcreate","comsvcs/IComInstanceEvents::OnObjectCreate","cos.icominstanceevents_onobjectcreate"]
old-location: cos\icominstanceevents_onobjectcreate.htm
tech.root: cos
ms.assetid: 4f3457f6-4956-4411-b38b-46c7d84d342d
ms.date: 12/05/2018
ms.keywords: IComInstanceEvents interface [COM+],OnObjectCreate method, IComInstanceEvents.OnObjectCreate, IComInstanceEvents::OnObjectCreate, OnObjectCreate, OnObjectCreate method [COM+], OnObjectCreate method [COM+],IComInstanceEvents interface, _dtc_icominstanceevents_onobjectcreate, comsvcs/IComInstanceEvents::OnObjectCreate, cos.icominstanceevents_onobjectcreate
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
 - IComInstanceEvents::OnObjectCreate
 - comsvcs/IComInstanceEvents::OnObjectCreate
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
 - IComInstanceEvents.OnObjectCreate
---

# IComInstanceEvents::OnObjectCreate


## -description

Generated when an object is created by a client.

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

The initial just-in-time (JIT) activated object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstanceevents">IComInstanceEvents</a>