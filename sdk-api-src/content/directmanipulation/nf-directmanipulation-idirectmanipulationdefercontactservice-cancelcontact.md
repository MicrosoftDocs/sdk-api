---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.CancelContact
title: IDirectManipulationDeferContactService::CancelContact (directmanipulation.h)
description: Cancel all scheduled calls to SetContact for this pointerId.
helpviewer_keywords: ["CancelContact","CancelContact method [Direct Manipulation]","CancelContact method [Direct Manipulation]","IDirectManipulationDeferContactService interface","IDirectManipulationDeferContactService interface [Direct Manipulation]","CancelContact method","IDirectManipulationDeferContactService.CancelContact","IDirectManipulationDeferContactService::CancelContact","directmanipulation.idirectmanipulationdefercontactservice_cancelcontact","directmanipulation/IDirectManipulationDeferContactService::CancelContact"]
old-location: directmanipulation\idirectmanipulationdefercontactservice_cancelcontact.htm
tech.root: directmanipulation
ms.assetid: 5C5029E5-CA4B-4853-B9D3-B99E869A44C3
ms.date: 12/05/2018
ms.keywords: CancelContact, CancelContact method [Direct Manipulation], CancelContact method [Direct Manipulation],IDirectManipulationDeferContactService interface, IDirectManipulationDeferContactService interface [Direct Manipulation],CancelContact method, IDirectManipulationDeferContactService.CancelContact, IDirectManipulationDeferContactService::CancelContact, directmanipulation.idirectmanipulationdefercontactservice_cancelcontact, directmanipulation/IDirectManipulationDeferContactService::CancelContact
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
 - IDirectManipulationDeferContactService::CancelContact
 - directmanipulation/IDirectManipulationDeferContactService::CancelContact
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
 - IDirectManipulationDeferContactService.CancelContact
---

# IDirectManipulationDeferContactService::CancelContact


## -description

Cancel all scheduled calls to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> for this <i>pointerId</i>.

## -parameters

### -param pointerId [in]

The ID of the pointer.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function fails if the timeout specified in <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact">DeferContact</a> has already been reached.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a>