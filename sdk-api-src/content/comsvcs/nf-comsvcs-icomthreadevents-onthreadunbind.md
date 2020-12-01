---
UID: NF:comsvcs.IComThreadEvents.OnThreadUnBind
title: IComThreadEvents::OnThreadUnBind (comsvcs.h)
description: Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.
helpviewer_keywords: ["IComThreadEvents interface [COM+]","OnThreadUnBind method","IComThreadEvents.OnThreadUnBind","IComThreadEvents::OnThreadUnBind","OnThreadUnBind","OnThreadUnBind method [COM+]","OnThreadUnBind method [COM+]","IComThreadEvents interface","_dtc_IComThreadEvents_OnThreadUnBind","comsvcs/IComThreadEvents::OnThreadUnBind","cos.icomthreadevents_onthreadunbind"]
old-location: cos\icomthreadevents_onthreadunbind.htm
tech.root: cos
ms.assetid: 21ce95a4-0e87-4e2d-a3fa-b21a079058e2
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadUnBind method, IComThreadEvents.OnThreadUnBind, IComThreadEvents::OnThreadUnBind, OnThreadUnBind, OnThreadUnBind method [COM+], OnThreadUnBind method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadUnBind, comsvcs/IComThreadEvents::OnThreadUnBind, cos.icomthreadevents_onthreadunbind
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
 - IComThreadEvents::OnThreadUnBind
 - comsvcs/IComThreadEvents::OnThreadUnBind
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
 - IComThreadEvents.OnThreadUnBind
---

# IComThreadEvents::OnThreadUnBind


## -description

Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ThreadID [in]

The unique thread identifier.

### -param AptID [in]

The apartment identifier.

### -param dwActCnt [in]

The number of current activities on the apartment thread.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>