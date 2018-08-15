---
UID: NF:directmanipulation.IDirectManipulationManager.CreateViewport
title: IDirectManipulationManager::CreateViewport
author: windows-sdk-content
description: The factory method that is used to create a new IDirectManipulationViewport object.
old-location: directmanipulation\idirectmanipulationmanager_createviewport.htm
old-project: directmanipulation
ms.assetid: 82a0146d-89c1-4672-93a9-e8f406b03d4e
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateViewport, CreateViewport method [Direct Manipulation], CreateViewport method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],CreateViewport method, IDirectManipulationManager.CreateViewport, IDirectManipulationManager::CreateViewport, directmanipulation.idirectmanipulationmanager_createviewport, directmanipulation/IDirectManipulationManager::CreateViewport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.CreateViewport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager::CreateViewport


## -description


The factory method that is used to create a new <a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a> object.

The viewport manages the interaction state and mapping of input to output actions.


## -parameters




### -param frameInfo [in, optional]

The frame info provider for the viewport.


### -param window [in]

The handle of the main app window to associate with the viewport.


### -param riid [in]

IID to the interface.


### -param object [out, retval]

The new <a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a> object.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

