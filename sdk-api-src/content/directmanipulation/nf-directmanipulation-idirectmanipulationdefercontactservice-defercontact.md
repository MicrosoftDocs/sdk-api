---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.DeferContact
title: IDirectManipulationDeferContactService::DeferContact (directmanipulation.h)
description: Specifies the amount of time to defer the execution of a call to SetContact for this pointerId.
helpviewer_keywords: ["DeferContact","DeferContact method [Direct Manipulation]","DeferContact method [Direct Manipulation]","IDirectManipulationDeferContactService interface","IDirectManipulationDeferContactService interface [Direct Manipulation]","DeferContact method","IDirectManipulationDeferContactService.DeferContact","IDirectManipulationDeferContactService::DeferContact","directmanipulation.idirectmanipulationdefercontactservice_defercontact","directmanipulation/IDirectManipulationDeferContactService::DeferContact"]
old-location: directmanipulation\idirectmanipulationdefercontactservice_defercontact.htm
tech.root: directmanipulation
ms.assetid: DEC97DD5-E43F-4541-8A80-D20EC8026493
ms.date: 12/05/2018
ms.keywords: DeferContact, DeferContact method [Direct Manipulation], DeferContact method [Direct Manipulation],IDirectManipulationDeferContactService interface, IDirectManipulationDeferContactService interface [Direct Manipulation],DeferContact method, IDirectManipulationDeferContactService.DeferContact, IDirectManipulationDeferContactService::DeferContact, directmanipulation.idirectmanipulationdefercontactservice_defercontact, directmanipulation/IDirectManipulationDeferContactService::DeferContact
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
 - IDirectManipulationDeferContactService::DeferContact
 - directmanipulation/IDirectManipulationDeferContactService::DeferContact
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
 - IDirectManipulationDeferContactService.DeferContact
---

# IDirectManipulationDeferContactService::DeferContact


## -description

Specifies the amount of time to defer the execution of a call to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> for this <i>pointerId</i>.

<b>DeferContact</b> must be called before <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a>.

## -parameters

### -param pointerId [in]

The ID of the pointer.

### -param timeout [in]

The duration of the deferral, in milliseconds. The maximum value is 500.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a>