---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnViewportStatusChanged
title: IDirectManipulationViewportEventHandler::OnViewportStatusChanged (directmanipulation.h)
description: Called when the status of a viewport changes.
helpviewer_keywords: ["IDirectManipulationViewportEventHandler interface [Direct Manipulation]","OnViewportStatusChanged method","IDirectManipulationViewportEventHandler.OnViewportStatusChanged","IDirectManipulationViewportEventHandler::OnViewportStatusChanged","OnViewportStatusChanged","OnViewportStatusChanged method [Direct Manipulation]","OnViewportStatusChanged method [Direct Manipulation]","IDirectManipulationViewportEventHandler interface","directmanipulation.idirectmanipulationviewporteventhandler_onviewportstatuschanged","directmanipulation/IDirectManipulationViewportEventHandler::OnViewportStatusChanged"]
old-location: directmanipulation\idirectmanipulationviewporteventhandler_onviewportstatuschanged.htm
tech.root: directmanipulation
ms.assetid: 7fe7106d-1b13-4a3e-8841-550e0ef55f95
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewportEventHandler interface [Direct Manipulation],OnViewportStatusChanged method, IDirectManipulationViewportEventHandler.OnViewportStatusChanged, IDirectManipulationViewportEventHandler::OnViewportStatusChanged, OnViewportStatusChanged, OnViewportStatusChanged method [Direct Manipulation], OnViewportStatusChanged method [Direct Manipulation],IDirectManipulationViewportEventHandler interface, directmanipulation.idirectmanipulationviewporteventhandler_onviewportstatuschanged, directmanipulation/IDirectManipulationViewportEventHandler::OnViewportStatusChanged
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
 - IDirectManipulationViewportEventHandler::OnViewportStatusChanged
 - directmanipulation/IDirectManipulationViewportEventHandler::OnViewportStatusChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directmanipulation.h
api_name:
 - IDirectManipulationViewportEventHandler.OnViewportStatusChanged
---

# IDirectManipulationViewportEventHandler::OnViewportStatusChanged


## -description

Called when the status of a viewport changes.

## -parameters

### -param viewport [in]

The viewport for which status has changed.

### -param current [in]

The new status of the viewport.

### -param previous [in]

The previous status of the viewport.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you call <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus">GetStatus</a> from within this handler, the status returned is not guaranteed to be the same as at the time of the call. This is because of the asynchronous nature of the notification.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler">IDirectManipulationViewportEventHandler</a>