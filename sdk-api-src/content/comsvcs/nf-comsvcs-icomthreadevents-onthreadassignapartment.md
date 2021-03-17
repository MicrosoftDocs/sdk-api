---
UID: NF:comsvcs.IComThreadEvents.OnThreadAssignApartment
title: IComThreadEvents::OnThreadAssignApartment (comsvcs.h)
description: Generated when an activity is assigned to an apartment thread.
helpviewer_keywords: ["IComThreadEvents interface [COM+]","OnThreadAssignApartment method","IComThreadEvents.OnThreadAssignApartment","IComThreadEvents::OnThreadAssignApartment","OnThreadAssignApartment","OnThreadAssignApartment method [COM+]","OnThreadAssignApartment method [COM+]","IComThreadEvents interface","_dtc_IComThreadEvents_OnThreadAssignApartment","comsvcs/IComThreadEvents::OnThreadAssignApartment","cos.icomthreadevents_onthreadassignapartment"]
old-location: cos\icomthreadevents_onthreadassignapartment.htm
tech.root: cos
ms.assetid: 2711b4b9-f27c-42c4-8f78-f31ffba2cfcf
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadAssignApartment method, IComThreadEvents.OnThreadAssignApartment, IComThreadEvents::OnThreadAssignApartment, OnThreadAssignApartment, OnThreadAssignApartment method [COM+], OnThreadAssignApartment method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadAssignApartment, comsvcs/IComThreadEvents::OnThreadAssignApartment, cos.icomthreadevents_onthreadassignapartment
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
 - IComThreadEvents::OnThreadAssignApartment
 - comsvcs/IComThreadEvents::OnThreadAssignApartment
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
 - IComThreadEvents.OnThreadAssignApartment
---

# IComThreadEvents::OnThreadAssignApartment


## -description

Generated when an activity is assigned to an apartment thread.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidActivity [in]

The activity identifier for which the object is created.

### -param AptID [in]

The apartment identifier.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>