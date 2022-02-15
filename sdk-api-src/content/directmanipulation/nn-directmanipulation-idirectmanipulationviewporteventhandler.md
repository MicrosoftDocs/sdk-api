---
UID: NN:directmanipulation.IDirectManipulationViewportEventHandler
title: IDirectManipulationViewportEventHandler (directmanipulation.h)
description: Defines methods for handling status and update events for the viewport.
helpviewer_keywords: ["IDirectManipulationViewportEventHandler","IDirectManipulationViewportEventHandler interface [Direct Manipulation]","IDirectManipulationViewportEventHandler interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationviewporteventhandler","directmanipulation/IDirectManipulationViewportEventHandler"]
old-location: directmanipulation\idirectmanipulationviewporteventhandler.htm
tech.root: directmanipulation
ms.assetid: 3594011a-da4a-4550-9b3b-076218d09f39
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewportEventHandler, IDirectManipulationViewportEventHandler interface [Direct Manipulation], IDirectManipulationViewportEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationviewporteventhandler, directmanipulation/IDirectManipulationViewportEventHandler
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
 - IDirectManipulationViewportEventHandler
 - directmanipulation/IDirectManipulationViewportEventHandler
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
 - IDirectManipulationViewportEventHandler
---

# IDirectManipulationViewportEventHandler interface


## -description

Defines methods for handling status and update events for the viewport.


<div class="alert"><b>Note</b>  When implementing a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> object, ensure that the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b>IDirectManipulationViewportEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationViewportEventHandler</b> also has these types of members:

## -remarks

Client apps implement this handler to receive status and update events for viewports. Use <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addeventhandler">AddEventHandler</a> to set the handler for a viewport. Each viewport can have more than one handler.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
