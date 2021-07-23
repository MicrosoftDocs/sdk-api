---
UID: NF:shobjidl.IHWEventHandler2.HandleEventWithHWND
title: IHWEventHandler2::HandleEventWithHWND (shobjidl.h)
description: Handles AutoPlay device events that contain content types that the application is not registered to handle. This method provides a handle to the owner window so that UI can be displayed if the process requires elevated privileges.
helpviewer_keywords: ["HandleEventWithHWND","HandleEventWithHWND method [Windows Shell]","HandleEventWithHWND method [Windows Shell]","IHWEventHandler2 interface","IHWEventHandler2 interface [Windows Shell]","HandleEventWithHWND method","IHWEventHandler2.HandleEventWithHWND","IHWEventHandler2::HandleEventWithHWND","_shell_IHWEventHandler2_HandleEventWithHWND","shell.IHWEventHandler2_HandleEventWithHWND","shobjidl/IHWEventHandler2::HandleEventWithHWND"]
old-location: shell\IHWEventHandler2_HandleEventWithHWND.htm
tech.root: shell
ms.assetid: 65720250-ace5-488d-9be7-33b07d7cc667
ms.date: 12/05/2018
ms.keywords: HandleEventWithHWND, HandleEventWithHWND method [Windows Shell], HandleEventWithHWND method [Windows Shell],IHWEventHandler2 interface, IHWEventHandler2 interface [Windows Shell],HandleEventWithHWND method, IHWEventHandler2.HandleEventWithHWND, IHWEventHandler2::HandleEventWithHWND, _shell_IHWEventHandler2_HandleEventWithHWND, shell.IHWEventHandler2_HandleEventWithHWND, shobjidl/IHWEventHandler2::HandleEventWithHWND
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IHWEventHandler2::HandleEventWithHWND
 - shobjidl/IHWEventHandler2::HandleEventWithHWND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IHWEventHandler2.HandleEventWithHWND
---

# IHWEventHandler2::HandleEventWithHWND


## -description

Handles AutoPlay device events that contain content types that the application is not registered to handle. This method provides a handle to the owner window so that UI can be displayed if the process requires elevated privileges.

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

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the AutoPlay dialog that was displayed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a handler is invoked and requires immediate privilege elevation in a new process, it requires an active parent window handle to display its consent UI. <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler-handleevent">IHWEventHandler::HandleEvent</a> cannot give a handle, so only a blinking taskbar appears. <b>IHWEventHandler2::HandleEventWithHWND</b> provides the HWND and enables the UI to be displayed.

Note that if the handler was launched by default instead of by direct user action, the HWND is not active and the dialog is not shown in the foreground.

The event types are not C/C++ language constants; they are literal text strings.