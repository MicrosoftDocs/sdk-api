---
UID: NF:directmanipulation.IDirectManipulationManager.Deactivate
title: IDirectManipulationManager::Deactivate (directmanipulation.h)
description: Deactivates Direct Manipulation for processing input and handling callbacks on the specified window.
helpviewer_keywords: ["Deactivate","Deactivate method [Direct Manipulation]","Deactivate method [Direct Manipulation]","IDirectManipulationManager interface","IDirectManipulationManager interface [Direct Manipulation]","Deactivate method","IDirectManipulationManager.Deactivate","IDirectManipulationManager::Deactivate","directmanipulation.idirectmanipulationmanager_deactivate","directmanipulation/IDirectManipulationManager::Deactivate"]
old-location: directmanipulation\idirectmanipulationmanager_deactivate.htm
tech.root: directmanipulation
ms.assetid: 7f80fe8a-e088-41fa-b72e-2b248307ac4a
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [Direct Manipulation], Deactivate method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],Deactivate method, IDirectManipulationManager.Deactivate, IDirectManipulationManager::Deactivate, directmanipulation.idirectmanipulationmanager_deactivate, directmanipulation/IDirectManipulationManager::Deactivate
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
 - IDirectManipulationManager::Deactivate
 - directmanipulation/IDirectManipulationManager::Deactivate
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
 - IDirectManipulationManager.Deactivate
---

# IDirectManipulationManager::Deactivate


## -description

Deactivates <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> for processing input and  handling callbacks on the specified window.

## -parameters

### -param window [in]

The window in which to deactivate input.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The manipulation manager is deactivated by default. The manager does not receive or respond to input until <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-activate">Activate</a> is called. The manipulation manager should be deactivated when the app does not receive or respond to input. For example, when the app is minimized.

Calls to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-activate">Activate</a> and <b>Deactivate</b> are reference counted.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>