---
UID: NF:comsvcs.IComMethodEvents.OnMethodException
title: IComMethodEvents::OnMethodException (comsvcs.h)
description: Generated when an object's method generates an exception. (IComMethodEvents.OnMethodException)
helpviewer_keywords: ["IComMethodEvents interface [COM+]","OnMethodException method","IComMethodEvents.OnMethodException","IComMethodEvents::OnMethodException","OnMethodException","OnMethodException method [COM+]","OnMethodException method [COM+]","IComMethodEvents interface","_dtc_IComMethodEvents_OnMethodException","comsvcs/IComMethodEvents::OnMethodException","cos.icommethodevents_onmethodexception"]
old-location: cos\icommethodevents_onmethodexception.htm
tech.root: cos
ms.assetid: b504a2db-0d18-42f1-8572-dc066c3e7740
ms.date: 12/05/2018
ms.keywords: IComMethodEvents interface [COM+],OnMethodException method, IComMethodEvents.OnMethodException, IComMethodEvents::OnMethodException, OnMethodException, OnMethodException method [COM+], OnMethodException method [COM+],IComMethodEvents interface, _dtc_IComMethodEvents_OnMethodException, comsvcs/IComMethodEvents::OnMethodException, cos.icommethodevents_onmethodexception
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
 - IComMethodEvents::OnMethodException
 - comsvcs/IComMethodEvents::OnMethodException
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
 - IComMethodEvents.OnMethodException
---

# IComMethodEvents::OnMethodException


## -description

Generated when an object's method generates an exception.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param oid [in]

The just-in-time (JIT) activated object.

### -param guidCid [in]

The CLSID for the object being called.

### -param guidRid [in]

The identifier of the method.

### -param iMeth [in]

The v-table index of the method.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a>
