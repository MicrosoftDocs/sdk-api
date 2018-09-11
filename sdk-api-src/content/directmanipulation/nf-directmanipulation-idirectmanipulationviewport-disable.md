---
UID: NF:directmanipulation.IDirectManipulationViewport.Disable
title: IDirectManipulationViewport::Disable
author: windows-sdk-content
description: Stops input processing by the viewport.
old-location: directmanipulation\idirectmanipulationviewport_disable.htm
tech.root: directmanipulation
ms.assetid: ac4f3cbe-2769-468e-abe3-07b76ada5d7e
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: Disable, Disable method [Direct Manipulation], Disable method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],Disable method, IDirectManipulationViewport.Disable, IDirectManipulationViewport::Disable, directmanipulation.idirectmanipulationviewport_disable, directmanipulation/IDirectManipulationViewport::Disable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.Disable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::Disable


## -description


Stops input processing by the viewport.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a viewport is disabled, it immediately stops all transforms and moves the content to the final location. 

Call this method when you want to modify multiple attributes atomically. This method can be called at any time. 

The viewport will not resume processing input until <a href="https://msdn.microsoft.com/47ebb502-26c6-4bff-8baf-bd825fc06755">Enable</a> is called. 


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pViewport->Disable();
```





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

