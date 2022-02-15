---
UID: NN:directmanipulation.IDirectManipulationContent
title: IDirectManipulationContent (directmanipulation.h)
description: Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.
helpviewer_keywords: ["IDirectManipulationContent","IDirectManipulationContent interface [Direct Manipulation]","IDirectManipulationContent interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationcontent","directmanipulation/IDirectManipulationContent"]
old-location: directmanipulation\idirectmanipulationcontent.htm
tech.root: directmanipulation
ms.assetid: 4d69a503-f998-4197-824f-4df48825c941
ms.date: 12/05/2018
ms.keywords: IDirectManipulationContent, IDirectManipulationContent interface [Direct Manipulation], IDirectManipulationContent interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcontent, directmanipulation/IDirectManipulationContent
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
 - IDirectManipulationContent
 - directmanipulation/IDirectManipulationContent
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
 - IDirectManipulationContent
---

# IDirectManipulationContent interface


## -description

Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.

The content has a set of transforms that controls the visual movement of the surface during manipulation and inertia.
<div class="alert"><b>Note</b>  When implementing a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> object, ensure that the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b>IDirectManipulationContent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationContent</b> also has these types of members:

## -remarks

The system provides an implementation of <b>IDirectManipulationContent</b>.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
