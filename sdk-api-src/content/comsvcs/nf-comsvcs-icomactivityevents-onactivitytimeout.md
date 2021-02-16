---
UID: NF:comsvcs.IComActivityEvents.OnActivityTimeout
title: IComActivityEvents::OnActivityTimeout (comsvcs.h)
description: Generated when a call into an activity times out.
helpviewer_keywords: ["IComActivityEvents interface [COM+]","OnActivityTimeout method","IComActivityEvents.OnActivityTimeout","IComActivityEvents::OnActivityTimeout","OnActivityTimeout","OnActivityTimeout method [COM+]","OnActivityTimeout method [COM+]","IComActivityEvents interface","_dtc_IComActivityEvents_OnActivityTimeout","comsvcs/IComActivityEvents::OnActivityTimeout","cos.icomactivityevents_onactivitytimeout"]
old-location: cos\icomactivityevents_onactivitytimeout.htm
tech.root: cos
ms.assetid: f097bea7-99a4-41eb-9518-834683d9402b
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityTimeout method, IComActivityEvents.OnActivityTimeout, IComActivityEvents::OnActivityTimeout, OnActivityTimeout, OnActivityTimeout method [COM+], OnActivityTimeout method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityTimeout, comsvcs/IComActivityEvents::OnActivityTimeout, cos.icomactivityevents_onactivitytimeout
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
 - IComActivityEvents::OnActivityTimeout
 - comsvcs/IComActivityEvents::OnActivityTimeout
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
 - IComActivityEvents.OnActivityTimeout
---

# IComActivityEvents::OnActivityTimeout


## -description

Generated when a call into an activity times out.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidCurrent [in]

The GUID associated with the current activity.

### -param guidEntered [in]

The causality identifier for the caller.

### -param dwThread [in]

The identifier of the  thread executing the call.

### -param dwTimeout [in]

The time-out period.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>