---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnContentUpdated
title: IDirectManipulationViewportEventHandler::OnContentUpdated (directmanipulation.h)
description: Called when content inside a viewport is updated.
helpviewer_keywords: ["IDirectManipulationViewportEventHandler interface [Direct Manipulation]","OnContentUpdated method","IDirectManipulationViewportEventHandler.OnContentUpdated","IDirectManipulationViewportEventHandler::OnContentUpdated","OnContentUpdated","OnContentUpdated method [Direct Manipulation]","OnContentUpdated method [Direct Manipulation]","IDirectManipulationViewportEventHandler interface","directmanipulation.idirectmanipulationviewporteventhandler_oncontentupdated","directmanipulation/IDirectManipulationViewportEventHandler::OnContentUpdated"]
old-location: directmanipulation\idirectmanipulationviewporteventhandler_oncontentupdated.htm
tech.root: directmanipulation
ms.assetid: 1b9a0f54-ccc7-4927-a34e-724652f6c2f0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewportEventHandler interface [Direct Manipulation],OnContentUpdated method, IDirectManipulationViewportEventHandler.OnContentUpdated, IDirectManipulationViewportEventHandler::OnContentUpdated, OnContentUpdated, OnContentUpdated method [Direct Manipulation], OnContentUpdated method [Direct Manipulation],IDirectManipulationViewportEventHandler interface, directmanipulation.idirectmanipulationviewporteventhandler_oncontentupdated, directmanipulation/IDirectManipulationViewportEventHandler::OnContentUpdated
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
 - IDirectManipulationViewportEventHandler::OnContentUpdated
 - directmanipulation/IDirectManipulationViewportEventHandler::OnContentUpdated
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
 - IDirectManipulationViewportEventHandler.OnContentUpdated
---

# IDirectManipulationViewportEventHandler::OnContentUpdated


## -description

Called when content inside a viewport is updated.

## -parameters

### -param viewport [in]

The viewport that is updated.

### -param content [in]

The content in the viewport that has changed.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called once for each  content change in the viewport. This can result in multiple <b>OnContentUpdated</b> calls. For instance, when the position of the content is changed, you can use <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-getcontenttransform">IDirectManipualtionContent::GetContentTransform</a> to retrieve the new value.

If you have actions that need to be executed once for a viewport update, implement <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewporteventhandler-onviewportupdated">OnViewportUpdated</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler">IDirectManipulationViewportEventHandler</a>