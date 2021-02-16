---
UID: NF:comsvcs.IMtsEvents.PostEvent
title: IMtsEvents::PostEvent (comsvcs.h)
description: Posts a user-defined event to an event sink.
helpviewer_keywords: ["IMtsEvents interface [COM+]","PostEvent method","IMtsEvents.PostEvent","IMtsEvents::PostEvent","PostEvent","PostEvent method [COM+]","PostEvent method [COM+]","IMtsEvents interface","_dtc_IMtsEvents_PostEvent","comsvcs/IMtsEvents::PostEvent","cos.imtsevents_postevent"]
old-location: cos\imtsevents_postevent.htm
tech.root: cos
ms.assetid: 4dcbe3d9-f81b-4014-a3b4-16706e691cb0
ms.date: 12/05/2018
ms.keywords: IMtsEvents interface [COM+],PostEvent method, IMtsEvents.PostEvent, IMtsEvents::PostEvent, PostEvent, PostEvent method [COM+], PostEvent method [COM+],IMtsEvents interface, _dtc_IMtsEvents_PostEvent, comsvcs/IMtsEvents::PostEvent, cos.imtsevents_postevent
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
 - IMtsEvents::PostEvent
 - comsvcs/IMtsEvents::PostEvent
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
 - IMtsEvents.PostEvent
---

# IMtsEvents::PostEvent


## -description

Posts a user-defined event to an event sink.

## -parameters

### -param vEvent [in]

A pointer to the name of the event.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>