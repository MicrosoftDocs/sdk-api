---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a handler is invoked and requires immediate privilege elevation in a new process, it requires an active parent window handle to display its consent UI. <a href="https://msdn.microsoft.com/575ca84c-8cf9-4ed6-a997-844cf0533986">IHWEventHandler::HandleEvent</a> cannot give a handle, so only a blinking taskbar appears. <b>IHWEventHandler2::HandleEventWithHWND</b> provides the HWND and enables the UI to be displayed.

Note that if the handler was launched by default instead of by direct user action, the HWND is not active and the dialog is not shown in the foreground.

The event types are not C/C++ language constants; they are literal text strings.



