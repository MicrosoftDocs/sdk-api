---
UID: NN:directmanipulation.IDirectManipulationViewport2
title: IDirectManipulationViewport2 (directmanipulation.h)
description: Provides management of behaviors on a viewport. A behavior affects the functionality of a particular part of the Direct Manipulation workflow.
helpviewer_keywords: ["IDirectManipulationViewport2","IDirectManipulationViewport2 interface [Direct Manipulation]","IDirectManipulationViewport2 interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationviewport2","directmanipulation/IDirectManipulationViewport2"]
old-location: directmanipulation\idirectmanipulationviewport2.htm
tech.root: directmanipulation
ms.assetid: 6EDFBA93-D2A2-4089-9976-CD1F8421B319
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport2, IDirectManipulationViewport2 interface [Direct Manipulation], IDirectManipulationViewport2 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationviewport2, directmanipulation/IDirectManipulationViewport2
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
 - IDirectManipulationViewport2
 - directmanipulation/IDirectManipulationViewport2
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
 - IDirectManipulationViewport2
---

# IDirectManipulationViewport2 interface


## -description

Provides management of behaviors on a viewport. A behavior affects the functionality of a particular part of the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> workflow.

## -inheritance

The <b>IDirectManipulationViewport2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>. <b>IDirectManipulationViewport2</b> also has these types of members:

## -remarks

<b>IDirectManipulationViewport2</b> can be used in place of <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>.


Behaviors are created using <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager2">IDirectManipulationManager2</a> and an appropriate class ID.

A behavior can be attached or removed at any time and takes effect immediately (even during an active manipulation or inertia animation).

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
