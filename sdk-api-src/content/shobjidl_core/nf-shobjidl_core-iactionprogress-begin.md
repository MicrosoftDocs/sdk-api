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

# IActionProgress::Begin


## -description


Called when an action has begun that requires its progress be displayed to the user.


## -parameters




### -param action [in]

Type: <b><a href="https://msdn.microsoft.com/fc5a0f96-e8c2-483f-86b0-d8c870a9f77a">SPACTION</a></b>

The action being performed. See <a href="https://msdn.microsoft.com/fc5a0f96-e8c2-483f-86b0-d8c870a9f77a">SPACTION</a> for a list of acceptable values.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/dc5215ca-17c8-47c1-8059-f46400ff1d0f">SPBEGINF</a></b>

Optional flags that request certain UI operations be enabled or disabled. See <a href="https://msdn.microsoft.com/dc5215ca-17c8-47c1-8059-f46400ff1d0f">SPBEGINF</a> for a list of acceptable values.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks




			This method should be called when an action is beginning. The values of <i>action</i> and <i>flags</i> may be used to determine how to draw the UI that will be displayed to the user, or how to interpret or filter certain user actions associated with the action. When the action has completed, <a href="https://msdn.microsoft.com/91fa11c3-c781-4e96-9a42-4625b8b24333">IActionProgress::End</a> should be called.
			




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/91fa11c3-c781-4e96-9a42-4625b8b24333">IActionProgress::End</a>



<a href="https://msdn.microsoft.com/fc5a0f96-e8c2-483f-86b0-d8c870a9f77a">SPACTION</a>



<a href="https://msdn.microsoft.com/dc5215ca-17c8-47c1-8059-f46400ff1d0f">SPBEGINF</a>
 

 

