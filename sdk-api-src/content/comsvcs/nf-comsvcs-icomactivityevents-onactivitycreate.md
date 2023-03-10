---
UID: NF:comsvcs.IComActivityEvents.OnActivityCreate
title: IComActivityEvents::OnActivityCreate (comsvcs.h)
description: Generated when an activity starts.
helpviewer_keywords: ["IComActivityEvents interface [COM+]","OnActivityCreate method","IComActivityEvents.OnActivityCreate","IComActivityEvents::OnActivityCreate","OnActivityCreate","OnActivityCreate method [COM+]","OnActivityCreate method [COM+]","IComActivityEvents interface","_dtc_IComActivityEvents_OnActivityCreate","comsvcs/IComActivityEvents::OnActivityCreate","cos.icomactivityevents_onactivitycreate"]
old-location: cos\icomactivityevents_onactivitycreate.htm
tech.root: cos
ms.assetid: 27d6dfd6-24c8-480b-9d91-6c6cce08384c
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityCreate method, IComActivityEvents.OnActivityCreate, IComActivityEvents::OnActivityCreate, OnActivityCreate, OnActivityCreate method [COM+], OnActivityCreate method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityCreate, comsvcs/IComActivityEvents::OnActivityCreate, cos.icomactivityevents_onactivitycreate
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
 - IComActivityEvents::OnActivityCreate
 - comsvcs/IComActivityEvents::OnActivityCreate
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
 - IComActivityEvents.OnActivityCreate
---

# IComActivityEvents::OnActivityCreate


## -description

Generated when an activity starts.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidActivity [in]

The GUID associated with the current activity.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>