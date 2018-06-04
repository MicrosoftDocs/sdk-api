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

# ISynchronizedInputProvider::StartListening


## -description


Starts listening for input of the specified type. 


## -parameters




### -param inputType [in]

Type: <b><a href="https://msdn.microsoft.com/28c66392-89f0-40eb-be19-ac84c64dacb7">SynchronizedInputType</a></b>

The type of input that is requested to be synchronized. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When it finds matching input, the provider checks if the target UI Automation element matches the current element. If they match, the provider raises the <a href="uiauto_event_ids.htm">UIA_InputReachedTargetEventId</a> event; otherwise, it raises the <a href="uiauto_event_ids.htm">UIA_InputReachedOtherElementEventId</a>  or <a href="uiauto_event_ids.htm">UIA_InputDiscardedEventId</a> event. The UI Automation provider must discard the input if it is for an element other than this one.

This is a one-shot method; after receiving input, the provider stops listening and continues normally.

This method returns E_INVALIDOPERATION if the provider is already listening for input.




## -see-also




<a href="https://msdn.microsoft.com/70495eba-172a-432e-951d-1092fd676d5e">ISynchronizedInputProvider</a>
 

 

