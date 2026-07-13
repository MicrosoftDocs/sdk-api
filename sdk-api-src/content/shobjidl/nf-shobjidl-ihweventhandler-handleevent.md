---
UID: NF:shobjidl.IHWEventHandler.HandleEvent
title: IHWEventHandler::HandleEvent (shobjidl.h)
description: Handles AutoPlay device events for which there is no content of the type the application is registered to handle.
helpviewer_keywords: ["HandleEvent","HandleEvent method [Windows Shell]","HandleEvent method [Windows Shell]","IHWEventHandler interface","IHWEventHandler interface [Windows Shell]","HandleEvent method","IHWEventHandler.HandleEvent","IHWEventHandler::HandleEvent","inet_IHWEventHandler_HandleEvent","shell.IHWEventHandler_HandleEvent","shobjidl/IHWEventHandler::HandleEvent"]
old-location: shell\IHWEventHandler_HandleEvent.htm
tech.root: shell
ms.assetid: 575ca84c-8cf9-4ed6-a997-844cf0533986
ms.date: 12/05/2018
ms.keywords: HandleEvent, HandleEvent method [Windows Shell], HandleEvent method [Windows Shell],IHWEventHandler interface, IHWEventHandler interface [Windows Shell],HandleEvent method, IHWEventHandler.HandleEvent, IHWEventHandler::HandleEvent, inet_IHWEventHandler_HandleEvent, shell.IHWEventHandler_HandleEvent, shobjidl/IHWEventHandler::HandleEvent
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shimgvw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHWEventHandler::HandleEvent
 - shobjidl/IHWEventHandler::HandleEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IHWEventHandler.HandleEvent
---

# IHWEventHandler::HandleEvent


## -description

Handles AutoPlay device events for which there is no content of the type the application is registered to handle.

## -parameters

### -param pszDeviceID [in]

Type: <b>LPCWSTR</b>

A pointer to a string buffer that contains the device ID.

### -param pszAltDeviceID [in]

Type: <b>LPCWSTR</b>

A pointer to a string buffer that contains the alternate device ID. The alternate device ID is more human-readable than the primary device ID.

### -param pszEventType [in]

Type: <b>LPCWSTR</b>

A pointer to a string buffer that contains the event type. The event types include DeviceArrival, DeviceRemoval, MediaArrival, and MediaRemoval.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The event types are not C/C++ language constants; they are literal text strings.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler-handleeventwithcontent">IHWEventHandler::HandleEventWithContent</a>