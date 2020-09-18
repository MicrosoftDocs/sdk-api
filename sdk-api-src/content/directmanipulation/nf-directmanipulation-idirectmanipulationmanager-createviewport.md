---
UID: NF:directmanipulation.IDirectManipulationManager.CreateViewport
title: IDirectManipulationManager::CreateViewport (directmanipulation.h)
description: The factory method that is used to create a new IDirectManipulationViewport object.
helpviewer_keywords: ["CreateViewport","CreateViewport method [Direct Manipulation]","CreateViewport method [Direct Manipulation]","IDirectManipulationManager interface","IDirectManipulationManager interface [Direct Manipulation]","CreateViewport method","IDirectManipulationManager.CreateViewport","IDirectManipulationManager::CreateViewport","directmanipulation.idirectmanipulationmanager_createviewport","directmanipulation/IDirectManipulationManager::CreateViewport"]
old-location: directmanipulation\idirectmanipulationmanager_createviewport.htm
tech.root: directmanipulation
ms.assetid: 82a0146d-89c1-4672-93a9-e8f406b03d4e
ms.date: 12/05/2018
ms.keywords: CreateViewport, CreateViewport method [Direct Manipulation], CreateViewport method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],CreateViewport method, IDirectManipulationManager.CreateViewport, IDirectManipulationManager::CreateViewport, directmanipulation.idirectmanipulationmanager_createviewport, directmanipulation/IDirectManipulationManager::CreateViewport
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
 - IDirectManipulationManager::CreateViewport
 - directmanipulation/IDirectManipulationManager::CreateViewport
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
 - IDirectManipulationManager.CreateViewport
---

# IDirectManipulationManager::CreateViewport


## -description

The factory method that is used to create a new <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a> object.

The viewport manages the interaction state and mapping of input to output actions.

## -parameters

### -param frameInfo [in, optional]

The frame info provider for the viewport.

### -param window [in]

The handle of the main app window to associate with the viewport.

### -param riid [in]

IID to the interface.

### -param object [out, retval]

The new <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a> object.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>