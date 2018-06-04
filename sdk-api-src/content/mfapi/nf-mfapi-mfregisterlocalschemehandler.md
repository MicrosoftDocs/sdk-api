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

# MFRegisterLocalSchemeHandler function


## -description


Registers a scheme handler in the caller's process.


## -parameters




### -param szScheme [in]

A string that contains the scheme. The scheme includes the trailing ':' character; for example, 
      "http:".


### -param pActivate [in]

A pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of an activation 
      object. The caller implements this interface. The 
      <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> 
      method of the activation object must create a scheme handler object. The scheme handler exposes the 
      <a href="https://msdn.microsoft.com/a342054e-2cb5-494a-a2f7-d144c72d1fa5">IMFSchemeHandler</a> interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Scheme handlers are used in Microsoft Media Foundation during the source resolution process, which creates a media 
    source from a URL. For more information, see 
    <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>.

Within a process, local scheme handlers take precedence over scheme handlers that are registered in the 
    registry. Local scheme handlers are not visible to other processes.

Use this function if you want to register a custom scheme handler for your application, but do not want the 
    handler available to other applications.




## -see-also




<a href="https://msdn.microsoft.com/B41FAA50-9CF7-4DD0-8571-1817C7C49276">MFRegisterLocalByteStreamHandler</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

