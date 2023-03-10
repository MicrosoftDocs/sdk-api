---
UID: NF:comsvcs.IComUserEvent.OnUserEvent
title: IComUserEvent::OnUserEvent (comsvcs.h)
description: Provided for user components to generate user-defined events.
helpviewer_keywords: ["IComUserEvent interface [COM+]","OnUserEvent method","IComUserEvent.OnUserEvent","IComUserEvent::OnUserEvent","OnUserEvent","OnUserEvent method [COM+]","OnUserEvent method [COM+]","IComUserEvent interface","_dtc_IComUserEvent_OnUserEvent","comsvcs/IComUserEvent::OnUserEvent","cos.icomuserevent_onuserevent"]
old-location: cos\icomuserevent_onuserevent.htm
tech.root: cos
ms.assetid: 3c14bf53-7466-4cb0-b90f-681796e40fd3
ms.date: 12/05/2018
ms.keywords: IComUserEvent interface [COM+],OnUserEvent method, IComUserEvent.OnUserEvent, IComUserEvent::OnUserEvent, OnUserEvent, OnUserEvent method [COM+], OnUserEvent method [COM+],IComUserEvent interface, _dtc_IComUserEvent_OnUserEvent, comsvcs/IComUserEvent::OnUserEvent, cos.icomuserevent_onuserevent
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
 - IComUserEvent::OnUserEvent
 - comsvcs/IComUserEvent::OnUserEvent
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
 - IComUserEvent.OnUserEvent
---

# IComUserEvent::OnUserEvent


## -description

Provided for user components to generate user-defined events.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param pvarEvent [in]

The user-defined information.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomuserevent">IComUserEvent</a>