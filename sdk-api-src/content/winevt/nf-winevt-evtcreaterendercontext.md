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

# EvtCreateRenderContext function


## -description


Creates a context that specifies the information in the event that you want to render.


## -parameters




### -param ValuePathsCount [in]

The number of XPath expressions in the <i>ValuePaths</i> parameter.


### -param ValuePaths [in]

An array of XPath expressions that uniquely identify a node or attribute in the event that you want to render. The expressions must not contain the <b>OR</b> or <b>AND</b> operator. Set to <b>NULL</b> if the <b>EvtRenderContextValues</b> context flag is not set in the <i>Flags</i> parameter.


### -param Flags [in]

One or more flags that identify the information in the event that you want to render. For example, the system information, user information, or specific values. For possible values, see the <a href="https://msdn.microsoft.com/1c933266-28d9-4ef2-b156-eedf4ccb189b">EVT_RENDER_CONTEXT_FLAGS</a> enumeration.


## -returns



A context handle that you use when calling the <a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a> function to render the contents of an event; otherwise, <b>NULL</b>. If <b>NULL</b>, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



To render the specified information from the event, call the  <a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a> function.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/fc763669-1fbc-4183-a4ff-577a7954d1ca">Rendering Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a>
 

 

