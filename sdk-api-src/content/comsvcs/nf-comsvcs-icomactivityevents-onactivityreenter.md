---
UID: NF:comsvcs.IComActivityEvents.OnActivityReenter
title: IComActivityEvents::OnActivityReenter (comsvcs.h)
description: Generated when an activity thread is reentered recursively.
helpviewer_keywords: ["IComActivityEvents interface [COM+]","OnActivityReenter method","IComActivityEvents.OnActivityReenter","IComActivityEvents::OnActivityReenter","OnActivityReenter","OnActivityReenter method [COM+]","OnActivityReenter method [COM+]","IComActivityEvents interface","_dtc_IComActivityEvents_OnActivityReenter","comsvcs/IComActivityEvents::OnActivityReenter","cos.icomactivityevents_onactivityreenter"]
old-location: cos\icomactivityevents_onactivityreenter.htm
tech.root: cos
ms.assetid: e055caab-379c-47c5-b62a-28ce5c2a0573
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityReenter method, IComActivityEvents.OnActivityReenter, IComActivityEvents::OnActivityReenter, OnActivityReenter, OnActivityReenter method [COM+], OnActivityReenter method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityReenter, comsvcs/IComActivityEvents::OnActivityReenter, cos.icomactivityevents_onactivityreenter
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
 - IComActivityEvents::OnActivityReenter
 - comsvcs/IComActivityEvents::OnActivityReenter
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
 - IComActivityEvents.OnActivityReenter
---

# IComActivityEvents::OnActivityReenter


## -description

Generated when an activity thread is reentered recursively.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidCurrent [in]

The GUID associated with the caller.

### -param dwThread [in]

The identifier of the activity thread.

### -param dwCallDepth [in]

The recursion depth.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>