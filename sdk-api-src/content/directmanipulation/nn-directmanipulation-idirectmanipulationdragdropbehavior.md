---
UID: NN:directmanipulation.IDirectManipulationDragDropBehavior
title: IDirectManipulationDragDropBehavior (directmanipulation.h)
description: Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures.
helpviewer_keywords: ["IDirectManipulationDragDropBehavior","IDirectManipulationDragDropBehavior interface [Direct Manipulation]","IDirectManipulationDragDropBehavior interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationdragdropbehavior","directmanipulation/IDirectManipulationDragDropBehavior"]
old-location: directmanipulation\idirectmanipulationdragdropbehavior.htm
tech.root: directmanipulation
ms.assetid: 99D99BB6-1DA1-4B49-88F8-16A9561A9098
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropBehavior, IDirectManipulationDragDropBehavior interface [Direct Manipulation], IDirectManipulationDragDropBehavior interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropbehavior, directmanipulation/IDirectManipulationDragDropBehavior
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
 - IDirectManipulationDragDropBehavior
 - directmanipulation/IDirectManipulationDragDropBehavior
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
 - IDirectManipulationDragDropBehavior
---

# IDirectManipulationDragDropBehavior interface


## -description

Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures. 

Call <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-addbehavior">AddBehavior</a> to apply the behavior on a viewport and <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-removebehavior">RemoveBehavior</a> to remove it.

## -inheritance

The <b>IDirectManipulationDragDropBehavior</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDragDropBehavior</b> also has these types of members:

## -remarks

If <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>, or <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a> has been called successfully on a viewport, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-addbehavior">AddBehavior</a> fails for the remaining lifetime of the viewport. 

Once the behavior is added to the viewport, calls to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>, or <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a> will fail until <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-removebehavior">RemoveBehavior</a> is called.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
