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

# WTSEnumerateListenersA function


## -description


Enumerates all the Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to 
      <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.


### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.


### -param pListeners [out, optional]

A pointer to an array of <b>WTSLISTENERNAME</b> variables that receive the names of 
      the listeners.


### -param pCount [in, out]

A pointer to a <b>DWORD</b> variable that contains the number of listener names in 
      the array referenced by the <i>pListeners</i> parameter. If the number of listener names is 
      unknown, pass <i>pListeners</i> as <b>NULL</b>. The function will return 
      the number of  <b>WTSLISTENERNAME</b> variables necessary to allocate for the array 
      pointed to by the <i>pListeners</i> parameter.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function  returns all listeners currently running on the server, including listeners that do not support 
    Remote Desktop Protocol (RDP).

If the number of listeners is unknown, you can call this function with <i>pListeners</i> 
    set to <b>NULL</b>. The function will then return, in the <i>pCount</i> 
    parameter, the number of <b>WTSLISTENERNAME</b> variables necessary to receive all the 
    listeners. Allocate the array for <i>pListeners</i> based on this number, and then call the 
    function again, setting <i>pListeners</i> to the newly allocated array and 
    <i>pCount</i> to the number returned by the first call.



