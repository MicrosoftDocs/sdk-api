---
UID: NN:directmanipulation.IDirectManipulationUpdateHandler
title: IDirectManipulationUpdateHandler (directmanipulation.h)
description: Defines methods for handling manipulation update events.
helpviewer_keywords: ["IDirectManipulationUpdateHandler","IDirectManipulationUpdateHandler interface [Direct Manipulation]","IDirectManipulationUpdateHandler interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationupdatehandler","directmanipulation/IDirectManipulationUpdateHandler"]
old-location: directmanipulation\idirectmanipulationupdatehandler.htm
tech.root: directmanipulation
ms.assetid: a963abb5-63b8-44d1-910c-ea795398d3de
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateHandler, IDirectManipulationUpdateHandler interface [Direct Manipulation], IDirectManipulationUpdateHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatehandler, directmanipulation/IDirectManipulationUpdateHandler
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
 - IDirectManipulationUpdateHandler
 - directmanipulation/IDirectManipulationUpdateHandler
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
 - IDirectManipulationUpdateHandler
---

# IDirectManipulationUpdateHandler interface


## -description

Defines methods for handling manipulation update events.


<div class="alert"><b>Note</b>  When implementing a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> object, ensure that the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b>IDirectManipulationUpdateHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationUpdateHandler</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
