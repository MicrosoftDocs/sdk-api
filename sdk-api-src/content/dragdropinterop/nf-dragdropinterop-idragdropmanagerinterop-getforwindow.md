---
UID: NF:dragdropinterop.IDragDropManagerInterop.GetForWindow
tech.root: winrt
title: IDragDropManagerInterop::GetForWindow
ms.date: 05/12/2021
targetos: Windows
description: Gets a CoreDragDropManager object for the window of the active application.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dragdropinterop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dragdropinterop.h
api_name:
 - IDragDropManagerInterop::GetForWindow
f1_keywords:
 - IDragDropManagerInterop::GetForWindow
 - dragdropinterop/IDragDropManagerInterop::GetForWindow
dev_langs:
 - c++
---

## -description

Gets a [CoreDragDropManager](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.coredragdropmanager) object for the window of the active application.

## -parameters

### -param hwnd

Handle to the window of the active application.

### -param riid

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example: 

`__uuidof(CoreDragDropManager)` 

### -param ppv

Address of a pointer to a [CoreDragDropManager](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.coredragdropmanager) object.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also

