---
UID: NF:directmanipulation.IDirectManipulationViewport.ReleaseAllContacts
title: IDirectManipulationViewport::ReleaseAllContacts (directmanipulation.h)
author: windows-sdk-content
description: Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.
old-location: directmanipulation\idirectmanipulationviewport_releaseallcontacts.htm
tech.root: directmanipulation
ms.assetid: 6ef43920-92bf-49c5-8e10-954d1b2b4440
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],ReleaseAllContacts method, IDirectManipulationViewport.ReleaseAllContacts, IDirectManipulationViewport::ReleaseAllContacts, ReleaseAllContacts, ReleaseAllContacts method [Direct Manipulation], ReleaseAllContacts method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_releaseallcontacts, directmanipulation/IDirectManipulationViewport::ReleaseAllContacts
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.ReleaseAllContacts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport::ReleaseAllContacts


## -description


Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This is equivalent to calling <a href="https://msdn.microsoft.com/fbb5cfba-4722-4470-aad5-2d192825244b">ReleaseContact</a> on every contact associated with the viewport. The outcome is equivalent to the user removing all touch points from the viewport. 

If supported, inertia will be started after calling this method.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

