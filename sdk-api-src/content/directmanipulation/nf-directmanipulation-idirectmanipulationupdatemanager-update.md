---
UID: NF:directmanipulation.IDirectManipulationUpdateManager.Update
title: IDirectManipulationUpdateManager::Update (directmanipulation.h)
description: Updates Direct Manipulation at the current time.
helpviewer_keywords: ["IDirectManipulationUpdateManager interface [Direct Manipulation]","Update method","IDirectManipulationUpdateManager.Update","IDirectManipulationUpdateManager::Update","Update","Update method [Direct Manipulation]","Update method [Direct Manipulation]","IDirectManipulationUpdateManager interface","directmanipulation.idirectmanipulationupdatemanager_update","directmanipulation/IDirectManipulationUpdateManager::Update"]
old-location: directmanipulation\idirectmanipulationupdatemanager_update.htm
tech.root: directmanipulation
ms.assetid: dffa747c-933a-4b61-9f15-e175d9338774
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateManager interface [Direct Manipulation],Update method, IDirectManipulationUpdateManager.Update, IDirectManipulationUpdateManager::Update, Update, Update method [Direct Manipulation], Update method [Direct Manipulation],IDirectManipulationUpdateManager interface, directmanipulation.idirectmanipulationupdatemanager_update, directmanipulation/IDirectManipulationUpdateManager::Update
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
 - IDirectManipulationUpdateManager::Update
 - directmanipulation/IDirectManipulationUpdateManager::Update
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
 - IDirectManipulationUpdateManager.Update
---

# IDirectManipulationUpdateManager::Update


## -description

Updates <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> at the current time.

## -parameters

### -param frameInfo [in, optional]

The frame info provider used to predict the position of the content and compensate for latency during composition.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the application provides its own implementation of <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>, this implementation should call <b>Update</b> whenever there is a compositor update. Frame timing information can be provided to <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> through the <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider">IDirectManipulationFrameInfoProvider</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">IDirectManipulationUpdateManager</a>