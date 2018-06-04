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

# UiaRemoveEvent function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Removes a listener for events on a node in the UI Automation tree.


## -parameters




### -param hEvent

TBD




#### - hevent [in]

Type: <b>HUIAEVENT</b>

The event to remove. This value was retrieved from <a href="https://msdn.microsoft.com/6d53c864-2791-4693-84dd-c7c1d8262b1f">UiaAddEvent</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The callback pointer, the scope, the node, and the list of properties must match exactly the parameters that were sent to the 
corresponding <a href="https://msdn.microsoft.com/6d53c864-2791-4693-84dd-c7c1d8262b1f">UiaAddEvent</a>.



