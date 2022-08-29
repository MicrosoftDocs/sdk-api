---
UID: NN:objidl.ISynchronizeEvent
title: ISynchronizeEvent (objidl.h)
description: The ISynchronizeEvent (objidl.h) interface assigns an event handle to a synchronization object.
helpviewer_keywords: ["ISynchronizeEvent","ISynchronizeEvent interface [COM]","ISynchronizeEvent interface [COM]","described","_com_isynchronizeevent","com.isynchronizeevent","objidlbase/ISynchronizeEvent"]
old-location: com\isynchronizeevent.htm
tech.root: com
ms.assetid: b4721498-0455-415a-bf2f-c8c8fdf3b75c
ms.date: 08/13/2022
ms.keywords: ISynchronizeEvent, ISynchronizeEvent interface [COM], ISynchronizeEvent interface [COM],described, _com_isynchronizeevent, com.isynchronizeevent, objidlbase/ISynchronizeEvent
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ISynchronizeEvent
 - objidl/ISynchronizeEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeEvent
---

# ISynchronizeEvent interface


## -description

Assigns an event handle to a synchronization object.

The synchronization object can use a handle to manage its activities. For example, the <a href="/windows/desktop/Sync/wait-functions">wait functions</a> use handles to identify the event they control. Thus, the logic of the <a href="/windows/desktop/api/objidl/nf-objidl-isynchronize-signal">ISynchronize::Signal</a> method on an event synchronization object can pass its handle to the <a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> function.

## -inheritance

The <b>ISynchronizeEvent</b> interface inherits from <b>ISynchronizeHandle</b>. <b>ISynchronizeEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizehandle">ISynchronizeHandle</a>
