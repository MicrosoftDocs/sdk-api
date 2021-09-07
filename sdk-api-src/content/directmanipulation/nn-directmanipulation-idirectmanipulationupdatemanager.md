---
UID: NN:directmanipulation.IDirectManipulationUpdateManager
title: IDirectManipulationUpdateManager (directmanipulation.h)
description: Manages how compositor updates are sent to Direct Manipulation.
helpviewer_keywords: ["IDirectManipulationUpdateManager","IDirectManipulationUpdateManager interface [Direct Manipulation]","IDirectManipulationUpdateManager interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationupdatemanager","directmanipulation/IDirectManipulationUpdateManager"]
old-location: directmanipulation\idirectmanipulationupdatemanager.htm
tech.root: directmanipulation
ms.assetid: 30626a22-1ded-49ff-a6c3-619a14d5ee3b
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateManager, IDirectManipulationUpdateManager interface [Direct Manipulation], IDirectManipulationUpdateManager interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatemanager, directmanipulation/IDirectManipulationUpdateManager
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
 - IDirectManipulationUpdateManager
 - directmanipulation/IDirectManipulationUpdateManager
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
 - IDirectManipulationUpdateManager
---

# IDirectManipulationUpdateManager interface


## -description

Manages how compositor updates are sent to <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

This interface enables the compositor to trigger an update on <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> whenever there is a compositor update. The application should not call the methods of this interface directly.

## -inheritance

The <b>IDirectManipulationUpdateManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationUpdateManager</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
