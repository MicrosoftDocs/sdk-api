---
UID: NF:directmanipulation.IDirectManipulationViewport.AddContent
title: IDirectManipulationViewport::AddContent (directmanipulation.h)
description: Adds secondary content, such as a panning indicator, to a viewport.
helpviewer_keywords: ["AddContent","AddContent method [Direct Manipulation]","AddContent method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","AddContent method","IDirectManipulationViewport.AddContent","IDirectManipulationViewport::AddContent","directmanipulation.idirectmanipulationviewport_addcontent","directmanipulation/IDirectManipulationViewport::AddContent"]
old-location: directmanipulation\idirectmanipulationviewport_addcontent.htm
tech.root: directmanipulation
ms.assetid: 1c404e9a-832d-47af-b162-2783faa05237
ms.date: 12/05/2018
ms.keywords: AddContent, AddContent method [Direct Manipulation], AddContent method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],AddContent method, IDirectManipulationViewport.AddContent, IDirectManipulationViewport::AddContent, directmanipulation.idirectmanipulationviewport_addcontent, directmanipulation/IDirectManipulationViewport::AddContent
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
 - IDirectManipulationViewport::AddContent
 - directmanipulation/IDirectManipulationViewport::AddContent
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
 - IDirectManipulationViewport.AddContent
---

# IDirectManipulationViewport::AddContent


## -description

Adds secondary content, such as a panning indicator, to a viewport.

## -parameters

### -param content [in]

The content to add to the viewport.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Secondary content is created by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-createcontent">CreateContent</a>. Once added, the secondary content will move relative to the primary content in response to a manipulation. Its motion is determined by rules associated with each type of secondary content.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>