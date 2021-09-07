---
UID: NF:directmanipulation.IDirectManipulationViewport.RemoveContent
title: IDirectManipulationViewport::RemoveContent (directmanipulation.h)
description: Removes secondary content from a viewport.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","RemoveContent method","IDirectManipulationViewport.RemoveContent","IDirectManipulationViewport::RemoveContent","RemoveContent","RemoveContent method [Direct Manipulation]","RemoveContent method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_removecontent","directmanipulation/IDirectManipulationViewport::RemoveContent"]
old-location: directmanipulation\idirectmanipulationviewport_removecontent.htm
tech.root: directmanipulation
ms.assetid: 5f7b709c-77ac-46fe-8fb5-dc4943824ab0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],RemoveContent method, IDirectManipulationViewport.RemoveContent, IDirectManipulationViewport::RemoveContent, RemoveContent, RemoveContent method [Direct Manipulation], RemoveContent method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_removecontent, directmanipulation/IDirectManipulationViewport::RemoveContent
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
 - IDirectManipulationViewport::RemoveContent
 - directmanipulation/IDirectManipulationViewport::RemoveContent
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
 - IDirectManipulationViewport.RemoveContent
---

# IDirectManipulationViewport::RemoveContent


## -description

Removes secondary content from a viewport.

## -parameters

### -param content [in]

The content object to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Secondary content can be removed from the viewport at any time.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>