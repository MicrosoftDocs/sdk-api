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
 

 

