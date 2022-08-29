---
UID: NF:objidl.ISynchronizeEvent.SetEventHandle
title: ISynchronizeEvent::SetEventHandle (objidl.h)
description: The ISynchronizeEvent::SetEventHandle method (objidl.h) assigns an event handle to a synchronization object.
helpviewer_keywords: ["ISynchronizeEvent interface [COM]","SetEventHandle method","ISynchronizeEvent.SetEventHandle","ISynchronizeEvent::SetEventHandle","SetEventHandle","SetEventHandle method [COM]","SetEventHandle method [COM]","ISynchronizeEvent interface","_com_isynchronizeevent_seteventhandle","com.isynchronizeevent_seteventhandle","objidlbase/ISynchronizeEvent::SetEventHandle"]
old-location: com\isynchronizeevent_seteventhandle.htm
tech.root: com
ms.assetid: e278930c-4f4d-4ac5-ba1e-a4a84bfcd0ca
ms.date: 08/15/2022
ms.keywords: ISynchronizeEvent interface [COM],SetEventHandle method, ISynchronizeEvent.SetEventHandle, ISynchronizeEvent::SetEventHandle, SetEventHandle, SetEventHandle method [COM], SetEventHandle method [COM],ISynchronizeEvent interface, _com_isynchronizeevent_seteventhandle, com.isynchronizeevent_seteventhandle, objidlbase/ISynchronizeEvent::SetEventHandle
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
 - ISynchronizeEvent::SetEventHandle
 - objidl/ISynchronizeEvent::SetEventHandle
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
 - ISynchronizeEvent.SetEventHandle
---

# ISynchronizeEvent::SetEventHandle


## -description

Assigns an event handle to a synchronization object.

## -parameters

### -param ph [in]

A pointer to the event handle.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

If the method is successful,
the object assumes ownership of the event handle,
and the caller should not close the handle.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizeevent">ISynchronizeEvent</a>
