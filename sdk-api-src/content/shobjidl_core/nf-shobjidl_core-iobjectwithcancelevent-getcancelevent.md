---
UID: NF:shobjidl_core.IObjectWithCancelEvent.GetCancelEvent
title: IObjectWithCancelEvent::GetCancelEvent (shobjidl_core.h)
description: Retrieves an event that will be sent when an operation is canceled.
helpviewer_keywords: ["GetCancelEvent","GetCancelEvent method [Windows Shell]","GetCancelEvent method [Windows Shell]","IObjectWithCancelEvent interface","IObjectWithCancelEvent interface [Windows Shell]","GetCancelEvent method","IObjectWithCancelEvent.GetCancelEvent","IObjectWithCancelEvent::GetCancelEvent","_shell_IObjectWithCancelEvent_GetCancelEvent","shell.IObjectWithCancelEvent_GetCancelEvent","shobjidl_core/IObjectWithCancelEvent::GetCancelEvent"]
old-location: shell\IObjectWithCancelEvent_GetCancelEvent.htm
tech.root: shell
ms.assetid: 6aef54b0-a7aa-4ff9-b50f-f84131614853
ms.date: 12/05/2018
ms.keywords: GetCancelEvent, GetCancelEvent method [Windows Shell], GetCancelEvent method [Windows Shell],IObjectWithCancelEvent interface, IObjectWithCancelEvent interface [Windows Shell],GetCancelEvent method, IObjectWithCancelEvent.GetCancelEvent, IObjectWithCancelEvent::GetCancelEvent, _shell_IObjectWithCancelEvent_GetCancelEvent, shell.IObjectWithCancelEvent_GetCancelEvent, shobjidl_core/IObjectWithCancelEvent::GetCancelEvent
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IObjectWithCancelEvent::GetCancelEvent
 - shobjidl_core/IObjectWithCancelEvent::GetCancelEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithCancelEvent.GetCancelEvent
---

# IObjectWithCancelEvent::GetCancelEvent


## -description

Retrieves an event that will be sent when an operation is canceled.

## -parameters

### -param phEvent [out]

Type: <b>HANDLE*</b>

Pointer to a handle that, when this method successfully returns, is the handle to the cancel event. The caller is responsible for closing this handle when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this function to retrieve an event that will be signaled when the called object cancels the operation it is performing. The caller is responsible for closing the returned handle.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent">IObjectWithCancelEvent</a>