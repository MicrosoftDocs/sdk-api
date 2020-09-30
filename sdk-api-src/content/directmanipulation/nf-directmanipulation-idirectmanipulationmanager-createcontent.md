---
UID: NF:directmanipulation.IDirectManipulationManager.CreateContent
title: IDirectManipulationManager::CreateContent (directmanipulation.h)
description: The factory method that is used to create an instance of secondary content (such as a panning indicator) inside a viewport.
helpviewer_keywords: ["CreateContent","CreateContent method [Direct Manipulation]","CreateContent method [Direct Manipulation]","IDirectManipulationManager interface","IDirectManipulationManager interface [Direct Manipulation]","CreateContent method","IDirectManipulationManager.CreateContent","IDirectManipulationManager::CreateContent","directmanipulation.idirectmanipulationmanager_createcontent","directmanipulation/IDirectManipulationManager::CreateContent"]
old-location: directmanipulation\idirectmanipulationmanager_createcontent.htm
tech.root: directmanipulation
ms.assetid: f8a2fbb2-f662-4eb7-88fb-64286205f19e
ms.date: 12/05/2018
ms.keywords: CreateContent, CreateContent method [Direct Manipulation], CreateContent method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],CreateContent method, IDirectManipulationManager.CreateContent, IDirectManipulationManager::CreateContent, directmanipulation.idirectmanipulationmanager_createcontent, directmanipulation/IDirectManipulationManager::CreateContent
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
 - IDirectManipulationManager::CreateContent
 - directmanipulation/IDirectManipulationManager::CreateContent
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
 - IDirectManipulationManager.CreateContent
---

# IDirectManipulationManager::CreateContent


## -description

The factory method that is used to create an instance of secondary content (such as a panning indicator) inside a viewport.

## -parameters

### -param frameInfo [in, optional]

The frame info provider for the secondary content. This should match the frame info provider used to create the viewport.

### -param clsid [in]

Class identifier (CLSID) of the secondary content. This ID specifies the content type.

### -param riid [in]

IID of the interface.

### -param object [out, retval]

The secondary content object that implements the specified interface.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Primary content is automatically created at the same time as the viewport and has a one-to-one relationship to a viewport. Therefore, it is not possible to create, add, or remove primary content.

Secondary content is created independently from the viewport. There is no limit to how much secondary content can be added or removed from a viewport. All secondary content transforms are derived from those supported by the primary content with specific rules applied based on the intended purpose of the element (identified by its Class identifier (CLSID)).

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>