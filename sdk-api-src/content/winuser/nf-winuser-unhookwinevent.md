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

# UnhookWinEvent function


## -description


Removes an event hook function created by a previous call to <a href="https://msdn.microsoft.com/090bda1b-0635-4aa3-ae33-3987b36e30b8">SetWinEventHook</a>.


## -parameters




### -param hWinEventHook [in]

Type: <b>HWINEVENTHOOK</b>

Handle to the event hook returned in the previous call to <a href="https://msdn.microsoft.com/090bda1b-0635-4aa3-ae33-3987b36e30b8">SetWinEventHook</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If successful, returns <b>TRUE</b>; otherwise, returns <b>FALSE</b>.

Three common errors cause this function to fail:

<ul>
<li>The <i>hWinEventHook</i> parameter is <b>NULL</b> or not valid.</li>
<li>The event hook specified by <i>hWinEventHook</i> was already removed.</li>
<li><b>UnhookWinEvent</b> is called from a thread that is different from the original call to <a href="https://msdn.microsoft.com/090bda1b-0635-4aa3-ae33-3987b36e30b8">SetWinEventHook</a>.</li>
</ul>



## -remarks



This function removes the event hook specified by <i>hWinEventHook</i> that prevents the corresponding callback function from receiving further event notifications. If the client's thread ends, the system automatically calls this function.

Call this function from the same thread that installed the event hook. <b>UnhookWinEvent</b> fails if called from a thread different from the call that corresponds to <a href="https://msdn.microsoft.com/090bda1b-0635-4aa3-ae33-3987b36e30b8">SetWinEventHook</a>.

If WINEVENT_INCONTEXT was specified when this event hook was installed, the system attempts to unload the corresponding DLL from all processes that loaded it. Although unloading does not occur immediately, the hook function is not called after <b>UnhookWinEvent</b> returns. For more information on WINEVENT_INCONTEXT, see <a href="https://msdn.microsoft.com/bf12bda6-b00e-4fbe-a576-b989aa428b54">In-Context Hook Functions</a>.



