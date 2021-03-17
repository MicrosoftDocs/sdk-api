---
UID: NF:directmanipulation.IDirectManipulationManager.GetUpdateManager
title: IDirectManipulationManager::GetUpdateManager (directmanipulation.h)
description: Gets a pointer to an IDirectManipulationUpdateManager object that receives compositor updates.
helpviewer_keywords: ["GetUpdateManager","GetUpdateManager method [Direct Manipulation]","GetUpdateManager method [Direct Manipulation]","IDirectManipulationManager interface","IDirectManipulationManager interface [Direct Manipulation]","GetUpdateManager method","IDirectManipulationManager.GetUpdateManager","IDirectManipulationManager::GetUpdateManager","directmanipulation.idirectmanipulationmanager_getupdatemanager","directmanipulation/IDirectManipulationManager::GetUpdateManager"]
old-location: directmanipulation\idirectmanipulationmanager_getupdatemanager.htm
tech.root: directmanipulation
ms.assetid: f3080fcb-3bbe-492b-a94e-322f93781cf5
ms.date: 12/05/2018
ms.keywords: GetUpdateManager, GetUpdateManager method [Direct Manipulation], GetUpdateManager method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],GetUpdateManager method, IDirectManipulationManager.GetUpdateManager, IDirectManipulationManager::GetUpdateManager, directmanipulation.idirectmanipulationmanager_getupdatemanager, directmanipulation/IDirectManipulationManager::GetUpdateManager
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
 - IDirectManipulationManager::GetUpdateManager
 - directmanipulation/IDirectManipulationManager::GetUpdateManager
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
 - IDirectManipulationManager.GetUpdateManager
---

# IDirectManipulationManager::GetUpdateManager


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">IDirectManipulationUpdateManager</a> object that receives compositor updates.

## -parameters

### -param riid [in]

IID to the interface.

### -param object [out, retval]

Pointer to the new <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">IDirectManipulationUpdateManager</a> object.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For the compositor to respond to update events from <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>, you must associate <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">IDirectManipulationUpdateManager</a> to an <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a> object during initialization. Use  <b>GetUpdateManager</b> to obtain a pointer to a <b>IDirectManipulationUpdateManager</b> object. Pass this pointer to the compositor using the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor-setupdatemanager">SetUpdateManager</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>