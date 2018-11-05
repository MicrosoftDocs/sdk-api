---
UID: NF:shobjidl.IHWEventHandler.HandleEvent
title: IHWEventHandler::HandleEvent
author: windows-sdk-content
description: Handles AutoPlay device events for which there is no content of the type the application is registered to handle.
old-location: shell\IHWEventHandler_HandleEvent.htm
tech.root: shell
ms.assetid: 575ca84c-8cf9-4ed6-a997-844cf0533986
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HandleEvent, HandleEvent method [Windows Shell], HandleEvent method [Windows Shell],IHWEventHandler interface, IHWEventHandler interface [Windows Shell],HandleEvent method, IHWEventHandler.HandleEvent, IHWEventHandler::HandleEvent, inet_IHWEventHandler_HandleEvent, shell.IHWEventHandler_HandleEvent, shobjidl/IHWEventHandler::HandleEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IHWEventHandler.HandleEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event types are not C/C++ language constants; they are literal text strings.




## -see-also




<a href="https://msdn.microsoft.com/be49322a-99b2-4626-8e9d-29965bbe182d">IHWEventHandler</a>



<a href="https://msdn.microsoft.com/d5787ebd-2784-4e86-b749-93258a1a26bd">IHWEventHandler::HandleEventWithContent</a>
 

 

