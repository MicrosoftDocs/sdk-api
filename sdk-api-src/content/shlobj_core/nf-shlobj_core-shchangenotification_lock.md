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

# SHChangeNotification_Lock function


## -description


Locks the shared memory associated with a Shell change notification event.


## -parameters




### -param hChange [in]

Type: <b>HANDLE</b>

A handle to a window received as a <i>wParam</i> in the specified Shell change notification message.


### -param dwProcId

Type: <b>DWORD</b>

The process ID (<i>lParam</i> in the message callback).


### -param pppidl [out, optional]

Type: <b>PIDLIST_ABSOLUTE**</b>

The address of a pointer to a PIDLIST_ABSOLUTE that, when this function returns successfully, receives the list of affected PIDLs.


### -param plEvent [out, optional]

Type: <b>LONG*</b>

A pointer to a LONG value that, when this function returns successfully, receives the Shell change notification ID of the event that took place.


## -returns



Type: <b>HANDLE</b>

Returns a handle (HLOCK) to the locked memory. Pass this value to <a href="https://msdn.microsoft.com/967ede1f-ee9c-46ee-a371-dcfc3a57d824">SHChangeNotification_Unlock</a> when finished.



