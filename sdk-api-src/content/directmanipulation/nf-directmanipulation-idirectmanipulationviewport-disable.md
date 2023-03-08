---
UID: NF:directmanipulation.IDirectManipulationViewport.Disable
title: IDirectManipulationViewport::Disable (directmanipulation.h)
description: Stops input processing by the viewport.
helpviewer_keywords: ["Disable","Disable method [Direct Manipulation]","Disable method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","Disable method","IDirectManipulationViewport.Disable","IDirectManipulationViewport::Disable","directmanipulation.idirectmanipulationviewport_disable","directmanipulation/IDirectManipulationViewport::Disable"]
old-location: directmanipulation\idirectmanipulationviewport_disable.htm
tech.root: directmanipulation
ms.assetid: ac4f3cbe-2769-468e-abe3-07b76ada5d7e
ms.date: 12/05/2018
ms.keywords: Disable, Disable method [Direct Manipulation], Disable method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],Disable method, IDirectManipulationViewport.Disable, IDirectManipulationViewport::Disable, directmanipulation.idirectmanipulationviewport_disable, directmanipulation/IDirectManipulationViewport::Disable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationViewport::Disable
 - directmanipulation/IDirectManipulationViewport::Disable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.Disable
---

# IDirectManipulationViewport::Disable


## -description

Stops input processing by the viewport.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a viewport is disabled, it immediately stops all transforms and moves the content to the final location. 

Call this method when you want to modify multiple attributes atomically. This method can be called at any time. 

The viewport will not resume processing input until <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-enable">Enable</a> is called. 


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pViewport->Disable();
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
