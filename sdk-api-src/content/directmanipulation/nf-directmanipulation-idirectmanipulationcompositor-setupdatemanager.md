---
UID: NF:directmanipulation.IDirectManipulationCompositor.SetUpdateManager
title: IDirectManipulationCompositor::SetUpdateManager (directmanipulation.h)
description: Sets the update manager used to send compositor updates to Direct Manipulation.
helpviewer_keywords: ["IDirectManipulationCompositor interface [Direct Manipulation]","SetUpdateManager method","IDirectManipulationCompositor.SetUpdateManager","IDirectManipulationCompositor::SetUpdateManager","SetUpdateManager","SetUpdateManager method [Direct Manipulation]","SetUpdateManager method [Direct Manipulation]","IDirectManipulationCompositor interface","directmanipulation.idirectmanipulationcompositor_setupdatemanager","directmanipulation/IDirectManipulationCompositor::SetUpdateManager"]
old-location: directmanipulation\idirectmanipulationcompositor_setupdatemanager.htm
tech.root: directmanipulation
ms.assetid: 8efab95b-2e06-4a3f-9b1b-171c1aada40a
ms.date: 12/05/2018
ms.keywords: IDirectManipulationCompositor interface [Direct Manipulation],SetUpdateManager method, IDirectManipulationCompositor.SetUpdateManager, IDirectManipulationCompositor::SetUpdateManager, SetUpdateManager, SetUpdateManager method [Direct Manipulation], SetUpdateManager method [Direct Manipulation],IDirectManipulationCompositor interface, directmanipulation.idirectmanipulationcompositor_setupdatemanager, directmanipulation/IDirectManipulationCompositor::SetUpdateManager
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
 - IDirectManipulationCompositor::SetUpdateManager
 - directmanipulation/IDirectManipulationCompositor::SetUpdateManager
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
 - IDirectManipulationCompositor.SetUpdateManager
---

# IDirectManipulationCompositor::SetUpdateManager


## -description

    Sets the update manager used to send compositor updates to <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

## -parameters

### -param updateManager [in]

The <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">update manager</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Retrieve <i>updateManager</i>  by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-getupdatemanager">GetUpdateManager</a>.

Call this method during <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> initialization to connect the compositor to the <i>update manager</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>