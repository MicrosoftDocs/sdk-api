---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolTimeout
title: IComObjectPoolEvents2::OnObjPoolTimeout (comsvcs.h)
description: Generated when the request for a pooled object times out.
helpviewer_keywords: ["IComObjectPoolEvents2 interface [COM+]","OnObjPoolTimeout method","IComObjectPoolEvents2.OnObjPoolTimeout","IComObjectPoolEvents2::OnObjPoolTimeout","OnObjPoolTimeout","OnObjPoolTimeout method [COM+]","OnObjPoolTimeout method [COM+]","IComObjectPoolEvents2 interface","_dtc_IComObjectPoolEvents2_OnObjPoolTimeout","comsvcs/IComObjectPoolEvents2::OnObjPoolTimeout","cos.icomobjectpoolevents2_onobjpooltimeout"]
old-location: cos\icomobjectpoolevents2_onobjpooltimeout.htm
tech.root: cos
ms.assetid: a5468ae6-6c7e-4ae1-afbc-24cc9b08102f
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolTimeout method, IComObjectPoolEvents2.OnObjPoolTimeout, IComObjectPoolEvents2::OnObjPoolTimeout, OnObjPoolTimeout, OnObjPoolTimeout method [COM+], OnObjPoolTimeout method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolTimeout, comsvcs/IComObjectPoolEvents2::OnObjPoolTimeout, cos.icomobjectpoolevents2_onobjpooltimeout
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
 - IComObjectPoolEvents2::OnObjPoolTimeout
 - comsvcs/IComObjectPoolEvents2::OnObjPoolTimeout
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
 - IComObjectPoolEvents2.OnObjPoolTimeout
---

# IComObjectPoolEvents2::OnObjPoolTimeout


## -description

Generated when the request for a pooled object times out.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param guidActivity [in]

The identifier of the activity in which the object is created.

### -param dwTimeout [in]

The pool's time-out value.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents2">IComObjectPoolEvents2</a>