---
UID: NF:directmanipulation.IDirectManipulationManager3.GetService
title: IDirectManipulationManager3::GetService (directmanipulation.h)
description: Retrieves an IDirectManipulationDeferContactService object.
helpviewer_keywords: ["GetService","GetService method [Direct Manipulation]","GetService method [Direct Manipulation]","IDirectManipulationManager3 interface","IDirectManipulationManager3 interface [Direct Manipulation]","GetService method","IDirectManipulationManager3.GetService","IDirectManipulationManager3::GetService","directmanipulation.idirectmanipulationmanager3_getservice","directmanipulation/IDirectManipulationManager3::GetService"]
old-location: directmanipulation\idirectmanipulationmanager3_getservice.htm
tech.root: directmanipulation
ms.assetid: 36f46402-ed71-41d8-8df5-02ef59819bb3
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Direct Manipulation], GetService method [Direct Manipulation],IDirectManipulationManager3 interface, IDirectManipulationManager3 interface [Direct Manipulation],GetService method, IDirectManipulationManager3.GetService, IDirectManipulationManager3::GetService, directmanipulation.idirectmanipulationmanager3_getservice, directmanipulation/IDirectManipulationManager3::GetService
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
 - IDirectManipulationManager3::GetService
 - directmanipulation/IDirectManipulationManager3::GetService
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
 - IDirectManipulationManager3.GetService
---

# IDirectManipulationManager3::GetService


## -description

Retrieves an <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a> object.

## -parameters

### -param clsid [in]

 The <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a> CLSID.

### -param riid [in]

The IID of the <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a> to retrieve.

### -param object [out, retval]

The <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a> object.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager3">IDirectManipulationManager3</a>