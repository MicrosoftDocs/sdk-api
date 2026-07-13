---
UID: NF:directmanipulation.IDirectManipulationViewport.Stop
title: IDirectManipulationViewport::Stop (directmanipulation.h)
description: Stops the manipulation and returns the viewport to a ready state.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","Stop method","IDirectManipulationViewport.Stop","IDirectManipulationViewport::Stop","Stop","Stop method [Direct Manipulation]","Stop method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_stop","directmanipulation/IDirectManipulationViewport::Stop"]
old-location: directmanipulation\idirectmanipulationviewport_stop.htm
tech.root: directmanipulation
ms.assetid: e0b88429-0d75-4c4a-8468-1a5637455324
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],Stop method, IDirectManipulationViewport.Stop, IDirectManipulationViewport::Stop, Stop, Stop method [Direct Manipulation], Stop method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_stop, directmanipulation/IDirectManipulationViewport::Stop
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
 - IDirectManipulationViewport::Stop
 - directmanipulation/IDirectManipulationViewport::Stop
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
 - IDirectManipulationViewport.Stop
---

# IDirectManipulationViewport::Stop


## -description

    Stops the manipulation and returns the viewport to a ready state.



## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If a mandatory snap point has been configured, the content may animate to the nearest snap point.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
