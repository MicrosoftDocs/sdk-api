---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.CancelDeferral
title: IDirectManipulationDeferContactService::CancelDeferral (directmanipulation.h)
description: Cancel the deferral set in DeferContact and process the scheduled SetContact call for this pointerId.
helpviewer_keywords: ["CancelDeferral","CancelDeferral method [Direct Manipulation]","CancelDeferral method [Direct Manipulation]","IDirectManipulationDeferContactService interface","IDirectManipulationDeferContactService interface [Direct Manipulation]","CancelDeferral method","IDirectManipulationDeferContactService.CancelDeferral","IDirectManipulationDeferContactService::CancelDeferral","directmanipulation.idirectmanipulationdefercontactservice_canceldeferral","directmanipulation/IDirectManipulationDeferContactService::CancelDeferral"]
old-location: directmanipulation\idirectmanipulationdefercontactservice_canceldeferral.htm
tech.root: directmanipulation
ms.assetid: 946F8CF8-6A6D-4BC1-B9BA-91D5B4A8A178
ms.date: 12/05/2018
ms.keywords: CancelDeferral, CancelDeferral method [Direct Manipulation], CancelDeferral method [Direct Manipulation],IDirectManipulationDeferContactService interface, IDirectManipulationDeferContactService interface [Direct Manipulation],CancelDeferral method, IDirectManipulationDeferContactService.CancelDeferral, IDirectManipulationDeferContactService::CancelDeferral, directmanipulation.idirectmanipulationdefercontactservice_canceldeferral, directmanipulation/IDirectManipulationDeferContactService::CancelDeferral
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
 - IDirectManipulationDeferContactService::CancelDeferral
 - directmanipulation/IDirectManipulationDeferContactService::CancelDeferral
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
 - IDirectManipulationDeferContactService.CancelDeferral
---

# IDirectManipulationDeferContactService::CancelDeferral


## -description

Cancel the deferral set in <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact">DeferContact</a> and process the scheduled <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> call for this <i>pointerId</i>.

## -parameters

### -param pointerId [in]

The ID of the pointer.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a>