---
UID: NF:directmanipulation.IDirectManipulationViewport.ReleaseAllContacts
title: IDirectManipulationViewport::ReleaseAllContacts (directmanipulation.h)
description: Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","ReleaseAllContacts method","IDirectManipulationViewport.ReleaseAllContacts","IDirectManipulationViewport::ReleaseAllContacts","ReleaseAllContacts","ReleaseAllContacts method [Direct Manipulation]","ReleaseAllContacts method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_releaseallcontacts","directmanipulation/IDirectManipulationViewport::ReleaseAllContacts"]
old-location: directmanipulation\idirectmanipulationviewport_releaseallcontacts.htm
tech.root: directmanipulation
ms.assetid: 6ef43920-92bf-49c5-8e10-954d1b2b4440
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],ReleaseAllContacts method, IDirectManipulationViewport.ReleaseAllContacts, IDirectManipulationViewport::ReleaseAllContacts, ReleaseAllContacts, ReleaseAllContacts method [Direct Manipulation], ReleaseAllContacts method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_releaseallcontacts, directmanipulation/IDirectManipulationViewport::ReleaseAllContacts
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
 - IDirectManipulationViewport::ReleaseAllContacts
 - directmanipulation/IDirectManipulationViewport::ReleaseAllContacts
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
 - IDirectManipulationViewport.ReleaseAllContacts
---

# IDirectManipulationViewport::ReleaseAllContacts


## -description

Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.



## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is equivalent to calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-releasecontact">ReleaseContact</a> on every contact associated with the viewport. The outcome is equivalent to the user removing all touch points from the viewport. 

If supported, inertia will be started after calling this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
