---
UID: NF:comsvcs.IComThreadEvents.OnThreadBindToApartment
title: IComThreadEvents::OnThreadBindToApartment (comsvcs.h)
description: Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in.
helpviewer_keywords: ["IComThreadEvents interface [COM+]","OnThreadBindToApartment method","IComThreadEvents.OnThreadBindToApartment","IComThreadEvents::OnThreadBindToApartment","OnThreadBindToApartment","OnThreadBindToApartment method [COM+]","OnThreadBindToApartment method [COM+]","IComThreadEvents interface","_dtc_IComThreadEvents_OnThreadBindToApartment","comsvcs/IComThreadEvents::OnThreadBindToApartment","cos.icomthreadevents_onthreadbindtoapartment"]
old-location: cos\icomthreadevents_onthreadbindtoapartment.htm
tech.root: cos
ms.assetid: d05c784a-5dcd-4155-baa0-775c499bd936
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadBindToApartment method, IComThreadEvents.OnThreadBindToApartment, IComThreadEvents::OnThreadBindToApartment, OnThreadBindToApartment, OnThreadBindToApartment method [COM+], OnThreadBindToApartment method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadBindToApartment, comsvcs/IComThreadEvents::OnThreadBindToApartment, cos.icomthreadevents_onthreadbindtoapartment
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
 - IComThreadEvents::OnThreadBindToApartment
 - comsvcs/IComThreadEvents::OnThreadBindToApartment
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
 - IComThreadEvents.OnThreadBindToApartment
---

# IComThreadEvents::OnThreadBindToApartment


## -description

Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in. An apartment thread is created or allocated from the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ThreadID [in]

The unique thread identifier.

### -param AptID [in]

The apartment identifier.

### -param dwActCnt [in]

The number of activities bound to this apartment.

### -param dwLowCnt [in]

This parameter is reserved.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>