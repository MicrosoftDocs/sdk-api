---
UID: NF:comsvcs.IComActivityEvents.OnActivityEnter
title: IComActivityEvents::OnActivityEnter (comsvcs.h)
description: Generated when an activity thread is entered.
helpviewer_keywords: ["IComActivityEvents interface [COM+]","OnActivityEnter method","IComActivityEvents.OnActivityEnter","IComActivityEvents::OnActivityEnter","OnActivityEnter","OnActivityEnter method [COM+]","OnActivityEnter method [COM+]","IComActivityEvents interface","_dtc_IComActivityEvents_OnActivityEnter","comsvcs/IComActivityEvents::OnActivityEnter","cos.icomactivityevents_onactivityenter"]
old-location: cos\icomactivityevents_onactivityenter.htm
tech.root: cos
ms.assetid: 5933798d-2208-4eab-8024-50236e5483a3
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityEnter method, IComActivityEvents.OnActivityEnter, IComActivityEvents::OnActivityEnter, OnActivityEnter, OnActivityEnter method [COM+], OnActivityEnter method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityEnter, comsvcs/IComActivityEvents::OnActivityEnter, cos.icomactivityevents_onactivityenter
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
 - IComActivityEvents::OnActivityEnter
 - comsvcs/IComActivityEvents::OnActivityEnter
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
 - IComActivityEvents.OnActivityEnter
---

# IComActivityEvents::OnActivityEnter


## -description

Generated when an activity thread is entered.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidCurrent [in]

The GUID associated with the caller.

### -param guidEntered [in]

The GUID associated with the activity thread entered.

### -param dwThread [in]

The identifier of the activity thread.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>