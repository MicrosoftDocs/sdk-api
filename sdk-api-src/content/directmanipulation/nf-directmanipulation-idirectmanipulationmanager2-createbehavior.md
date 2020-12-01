---
UID: NF:directmanipulation.IDirectManipulationManager2.CreateBehavior
title: IDirectManipulationManager2::CreateBehavior (directmanipulation.h)
description: Factory method to create a behavior.
helpviewer_keywords: ["CreateBehavior","CreateBehavior method [Direct Manipulation]","CreateBehavior method [Direct Manipulation]","IDirectManipulationManager2 interface","IDirectManipulationManager2 interface [Direct Manipulation]","CreateBehavior method","IDirectManipulationManager2.CreateBehavior","IDirectManipulationManager2::CreateBehavior","directmanipulation.idirectmanipulationmanager2_createbehavior","directmanipulation/IDirectManipulationManager2::CreateBehavior"]
old-location: directmanipulation\idirectmanipulationmanager2_createbehavior.htm
tech.root: directmanipulation
ms.assetid: 8890E44F-595A-4116-B4A4-F10FAEE598B7
ms.date: 12/05/2018
ms.keywords: CreateBehavior, CreateBehavior method [Direct Manipulation], CreateBehavior method [Direct Manipulation],IDirectManipulationManager2 interface, IDirectManipulationManager2 interface [Direct Manipulation],CreateBehavior method, IDirectManipulationManager2.CreateBehavior, IDirectManipulationManager2::CreateBehavior, directmanipulation.idirectmanipulationmanager2_createbehavior, directmanipulation/IDirectManipulationManager2::CreateBehavior
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
 - IDirectManipulationManager2::CreateBehavior
 - directmanipulation/IDirectManipulationManager2::CreateBehavior
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
 - IDirectManipulationManager2.CreateBehavior
---

# IDirectManipulationManager2::CreateBehavior


## -description

Factory method to create a behavior.

## -parameters

### -param clsid [in]

CLSID of the behavior. The CLSID specifies the type of behavior.

### -param riid [in]

The IID of the behavior interface to create.

### -param object [out, retval]

The new behavior object that implements the specified interface.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager2">IDirectManipulationManager2</a>