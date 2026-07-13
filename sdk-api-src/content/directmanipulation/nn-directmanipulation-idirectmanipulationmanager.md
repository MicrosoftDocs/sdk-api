---
UID: NN:directmanipulation.IDirectManipulationManager
title: IDirectManipulationManager (directmanipulation.h)
description: Provides access to all the Direct Manipulation features and APIs available to the client application.
helpviewer_keywords: ["IDirectManipulationManager","IDirectManipulationManager interface [Direct Manipulation]","IDirectManipulationManager interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationmanager","directmanipulation/IDirectManipulationManager"]
old-location: directmanipulation\idirectmanipulationmanager.htm
tech.root: directmanipulation
ms.assetid: d730a446-984e-4be0-aa7f-6d3dc93b2e34
ms.date: 12/05/2018
ms.keywords: IDirectManipulationManager, IDirectManipulationManager interface [Direct Manipulation], IDirectManipulationManager interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager, directmanipulation/IDirectManipulationManager
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
 - IDirectManipulationManager
 - directmanipulation/IDirectManipulationManager
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
 - IDirectManipulationManager
---

# IDirectManipulationManager interface


## -description

Provides access to all the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> features and APIs available to the client application.



This is the first COM object (the object factory) created by the application to retrieve other COM objects in the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> API surface. It also serves to activate and deactivate Direct Manipulation functionality on a per-HWND basis.

## -inheritance

The <b>IDirectManipulationManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationManager</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
