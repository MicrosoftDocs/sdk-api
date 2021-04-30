---
UID: NF:comsvcs.IComThreadEvents.OnThreadUnassignApartment
title: IComThreadEvents::OnThreadUnassignApartment (comsvcs.h)
description: Generated when an activity is unassigned from an apartment thread.
helpviewer_keywords: ["IComThreadEvents interface [COM+]","OnThreadUnassignApartment method","IComThreadEvents.OnThreadUnassignApartment","IComThreadEvents::OnThreadUnassignApartment","OnThreadUnassignApartment","OnThreadUnassignApartment method [COM+]","OnThreadUnassignApartment method [COM+]","IComThreadEvents interface","_dtc_IComThreadEvents_OnThreadUnassignApartment","comsvcs/IComThreadEvents::OnThreadUnassignApartment","cos.icomthreadevents_onthreadunassignapartment"]
old-location: cos\icomthreadevents_onthreadunassignapartment.htm
tech.root: cos
ms.assetid: c57b2427-9c39-4068-b531-9f18264746a1
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadUnassignApartment method, IComThreadEvents.OnThreadUnassignApartment, IComThreadEvents::OnThreadUnassignApartment, OnThreadUnassignApartment, OnThreadUnassignApartment method [COM+], OnThreadUnassignApartment method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadUnassignApartment, comsvcs/IComThreadEvents::OnThreadUnassignApartment, cos.icomthreadevents_onthreadunassignapartment
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
 - IComThreadEvents::OnThreadUnassignApartment
 - comsvcs/IComThreadEvents::OnThreadUnassignApartment
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
 - IComThreadEvents.OnThreadUnassignApartment
---

# IComThreadEvents::OnThreadUnassignApartment


## -description

Generated when an activity is unassigned from an apartment thread.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param AptID [in]

The apartment identifier.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>