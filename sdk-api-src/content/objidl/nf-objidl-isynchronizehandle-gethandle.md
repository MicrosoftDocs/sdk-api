---
UID: NF:objidl.ISynchronizeHandle.GetHandle
title: ISynchronizeHandle::GetHandle (objidl.h)
description: Retrieves a handle to the synchronization object.
helpviewer_keywords: ["GetHandle","GetHandle method [COM]","GetHandle method [COM]","ISynchronizeHandle interface","ISynchronizeHandle interface [COM]","GetHandle method","ISynchronizeHandle.GetHandle","ISynchronizeHandle::GetHandle","_com_isynchronizehandle_gethandle","com.isynchronizehandle_gethandle","objidlbase/ISynchronizeHandle::GetHandle"]
old-location: com\isynchronizehandle_gethandle.htm
tech.root: com
ms.assetid: 951bc2e4-2ef9-48cf-91a1-1a39c2361f42
ms.date: 12/05/2018
ms.keywords: GetHandle, GetHandle method [COM], GetHandle method [COM],ISynchronizeHandle interface, ISynchronizeHandle interface [COM],GetHandle method, ISynchronizeHandle.GetHandle, ISynchronizeHandle::GetHandle, _com_isynchronizehandle_gethandle, com.isynchronizehandle_gethandle, objidlbase/ISynchronizeHandle::GetHandle
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
 - ISynchronizeHandle::GetHandle
 - objidl/ISynchronizeHandle::GetHandle
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
 - ISynchronizeHandle.GetHandle
---

# ISynchronizeHandle::GetHandle


## -description

Retrieves a handle to the synchronization object.

## -parameters

### -param ph [out]

A pointer to the variable that receives a handle to the synchronization object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

Do not close the handle returned in the <i>ph</i> parameter.
The lifetime of the handle is controlled by the object that implements the ISynchronizeHandle interface.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isynchronizeevent-seteventhandle">ISynchronizeEvent::SetEventHandle</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizehandle">ISynchronizeHandle</a>