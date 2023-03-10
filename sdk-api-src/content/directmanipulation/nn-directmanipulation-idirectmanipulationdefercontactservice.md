---
UID: NN:directmanipulation.IDirectManipulationDeferContactService
title: IDirectManipulationDeferContactService (directmanipulation.h)
description: Represents a service for managing associations between a contact and a viewport.
helpviewer_keywords: ["IDirectManipulationDeferContactService","IDirectManipulationDeferContactService interface [Direct Manipulation]","IDirectManipulationDeferContactService interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationdefercontactservice","directmanipulation/IDirectManipulationDeferContactService"]
old-location: directmanipulation\idirectmanipulationdefercontactservice.htm
tech.root: directmanipulation
ms.assetid: 6063352F-39FF-4E8F-B836-3DA0A02BE523
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDeferContactService, IDirectManipulationDeferContactService interface [Direct Manipulation], IDirectManipulationDeferContactService interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdefercontactservice, directmanipulation/IDirectManipulationDeferContactService
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDirectManipulationDeferContactService
 - directmanipulation/IDirectManipulationDeferContactService
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
 - IDirectManipulationDeferContactService
---

# IDirectManipulationDeferContactService interface


## -description

Represents a service for managing associations between a contact and a viewport.


<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is called when a <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> message is received. Upon receiving a <b>WM_POINTERDOWN</b>, the application can use the coordinates of the input to hit-test and determine the viewports to which the contact is associated.

## -inheritance

The <b>IDirectManipulationDeferContactService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDeferContactService</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a>
