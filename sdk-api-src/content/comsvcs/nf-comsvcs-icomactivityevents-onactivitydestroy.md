---
UID: NF:comsvcs.IComActivityEvents.OnActivityDestroy
title: IComActivityEvents::OnActivityDestroy (comsvcs.h)
description: Generated when an activity is finished.helpviewer_keywords: ["IComActivityEvents interface [COM+]","OnActivityDestroy method","IComActivityEvents.OnActivityDestroy","IComActivityEvents::OnActivityDestroy","OnActivityDestroy","OnActivityDestroy method [COM+]","OnActivityDestroy method [COM+]","IComActivityEvents interface","_dtc_IComActivityEvents_OnActivityDestroy","comsvcs/IComActivityEvents::OnActivityDestroy","cos.icomactivityevents_onactivitydestroy"]
old-location: cos\icomactivityevents_onactivitydestroy.htm
tech.root: cossdk
ms.assetid: af69bcf7-a925-42e2-a7a8-4ebf745955b9
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityDestroy method, IComActivityEvents.OnActivityDestroy, IComActivityEvents::OnActivityDestroy, OnActivityDestroy, OnActivityDestroy method [COM+], OnActivityDestroy method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityDestroy, comsvcs/IComActivityEvents::OnActivityDestroy, cos.icomactivityevents_onactivitydestroy
f1_keywords:
- comsvcs/IComActivityEvents.OnActivityDestroy
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IComActivityEvents.OnActivityDestroy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComActivityEvents::OnActivityDestroy


## -description


Generated when an activity is finished.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The GUID associated with the current activity.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>
 

 

