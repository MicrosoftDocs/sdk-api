---
UID: NF:directmanipulation.IDirectManipulationViewport2.RemoveAllBehaviors
title: IDirectManipulationViewport2::RemoveAllBehaviors (directmanipulation.h)
description: Removes all behaviors added to the viewport.
helpviewer_keywords: ["IDirectManipulationViewport2 interface [Direct Manipulation]","RemoveAllBehaviors method","IDirectManipulationViewport2.RemoveAllBehaviors","IDirectManipulationViewport2::RemoveAllBehaviors","RemoveAllBehaviors","RemoveAllBehaviors method [Direct Manipulation]","RemoveAllBehaviors method [Direct Manipulation]","IDirectManipulationViewport2 interface","directmanipulation.idirectmanipulationviewport2_removeallbehaviors","directmanipulation/IDirectManipulationViewport2::RemoveAllBehaviors"]
old-location: directmanipulation\idirectmanipulationviewport2_removeallbehaviors.htm
tech.root: directmanipulation
ms.assetid: 94CCF2F4-F6E7-4446-8F6A-3E058B98A328
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport2 interface [Direct Manipulation],RemoveAllBehaviors method, IDirectManipulationViewport2.RemoveAllBehaviors, IDirectManipulationViewport2::RemoveAllBehaviors, RemoveAllBehaviors, RemoveAllBehaviors method [Direct Manipulation], RemoveAllBehaviors method [Direct Manipulation],IDirectManipulationViewport2 interface, directmanipulation.idirectmanipulationviewport2_removeallbehaviors, directmanipulation/IDirectManipulationViewport2::RemoveAllBehaviors
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDirectManipulationViewport2::RemoveAllBehaviors
 - directmanipulation/IDirectManipulationViewport2::RemoveAllBehaviors
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
 - IDirectManipulationViewport2.RemoveAllBehaviors
---

# IDirectManipulationViewport2::RemoveAllBehaviors


## -description

Removes all behaviors added to the viewport.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>RemoveAllBehaviors</b> only returns an error if the removal of a behavior from the viewport was unsuccessful. In the event that a specific behavior is not removed successfully, <b>RemoveAllBehaviors</b> removes all remaining behaviors.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport2">IDirectManipulationViewport2</a>
