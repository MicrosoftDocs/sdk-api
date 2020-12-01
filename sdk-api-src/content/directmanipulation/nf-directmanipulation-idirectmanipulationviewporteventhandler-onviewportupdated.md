---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnViewportUpdated
title: IDirectManipulationViewportEventHandler::OnViewportUpdated (directmanipulation.h)
description: Called after all content in the viewport has been updated.
helpviewer_keywords: ["IDirectManipulationViewportEventHandler interface [Direct Manipulation]","OnViewportUpdated method","IDirectManipulationViewportEventHandler.OnViewportUpdated","IDirectManipulationViewportEventHandler::OnViewportUpdated","OnViewportUpdated","OnViewportUpdated method [Direct Manipulation]","OnViewportUpdated method [Direct Manipulation]","IDirectManipulationViewportEventHandler interface","directmanipulation.idirectmanipulationviewporteventhandler_onviewportupdated","directmanipulation/IDirectManipulationViewportEventHandler::OnViewportUpdated"]
old-location: directmanipulation\idirectmanipulationviewporteventhandler_onviewportupdated.htm
tech.root: directmanipulation
ms.assetid: dfb70d6f-ce3c-4d39-b7b5-21812ff7e56b
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewportEventHandler interface [Direct Manipulation],OnViewportUpdated method, IDirectManipulationViewportEventHandler.OnViewportUpdated, IDirectManipulationViewportEventHandler::OnViewportUpdated, OnViewportUpdated, OnViewportUpdated method [Direct Manipulation], OnViewportUpdated method [Direct Manipulation],IDirectManipulationViewportEventHandler interface, directmanipulation.idirectmanipulationviewporteventhandler_onviewportupdated, directmanipulation/IDirectManipulationViewportEventHandler::OnViewportUpdated
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
 - IDirectManipulationViewportEventHandler::OnViewportUpdated
 - directmanipulation/IDirectManipulationViewportEventHandler::OnViewportUpdated
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
 - IDirectManipulationViewportEventHandler.OnViewportUpdated
---

# IDirectManipulationViewportEventHandler::OnViewportUpdated


## -description

Called after all content in the viewport has been updated.

## -parameters

### -param viewport [in]

The viewport that has been updated.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you have actions that need to be executed once for a viewport update, implement <b>OnViewportUpdated</b>. <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewporteventhandler-oncontentupdated">OnContentUpdated</a> is called once for each  content change in the viewport. This can result in multiple <b>OnContentUpdated</b> calls.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler">IDirectManipulationViewportEventHandler</a>