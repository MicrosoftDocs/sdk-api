---
UID: NF:directmanipulation.IDirectManipulationManager.RegisterHitTestTarget
title: IDirectManipulationManager::RegisterHitTestTarget (directmanipulation.h)
description: Registers a dedicated thread for hit testing.
helpviewer_keywords: ["IDirectManipulationManager interface [Direct Manipulation]","RegisterHitTestTarget method","IDirectManipulationManager.RegisterHitTestTarget","IDirectManipulationManager::RegisterHitTestTarget","RegisterHitTestTarget","RegisterHitTestTarget method [Direct Manipulation]","RegisterHitTestTarget method [Direct Manipulation]","IDirectManipulationManager interface","directmanipulation.idirectmanipulationmanager_registerhittesttarget","directmanipulation/IDirectManipulationManager::RegisterHitTestTarget"]
old-location: directmanipulation\idirectmanipulationmanager_registerhittesttarget.htm
tech.root: directmanipulation
ms.assetid: ba71a959-b9b9-4466-9239-f3c486f5e7b3
ms.date: 12/05/2018
ms.keywords: IDirectManipulationManager interface [Direct Manipulation],RegisterHitTestTarget method, IDirectManipulationManager.RegisterHitTestTarget, IDirectManipulationManager::RegisterHitTestTarget, RegisterHitTestTarget, RegisterHitTestTarget method [Direct Manipulation], RegisterHitTestTarget method [Direct Manipulation],IDirectManipulationManager interface, directmanipulation.idirectmanipulationmanager_registerhittesttarget, directmanipulation/IDirectManipulationManager::RegisterHitTestTarget
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
 - IDirectManipulationManager::RegisterHitTestTarget
 - directmanipulation/IDirectManipulationManager::RegisterHitTestTarget
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
 - IDirectManipulationManager.RegisterHitTestTarget
---

# IDirectManipulationManager::RegisterHitTestTarget


## -description

Registers a dedicated thread for hit testing.

## -parameters

### -param window [in]

The handle of the main app window (typically created from the UI thread).

### -param hitTestWindow [in, optional]

The handle of the window in which hit testing is registered (should be created from the hit testing thread). Pass in nullptr to unregister a previously registered hit-test target.

### -param type [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type">DIRECTMANIPULATION_HITTEST_TYPE</a>. Specifies whether the UI window or the hit testing window (or both) receives the hit testing <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> message , and in what order.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Hit testing is typically performed on the application UI thread. The application receives a <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> message on which hit-testing is performed. If a manipulation is required, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is called on one or more viewports. An application can use the <b>RegisterHitTestTarget</b> method to delegate this hit-testing responsibility to a separate hit-testing thread.


Once a dedicated hit-test target is successfully registered, <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages are processed on the hit-testing thread. If a manipulation, such as pan or zoom, is required, <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is called from this thread.


If <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is not called from the hit-testing thread, <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages may be processed on the UI thread, depending on the <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type">DIRECTMANIPULATION_HITTEST_TYPE</a> specified during registration.


If <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is not called by either the hit-test thread or the UI thread, <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> ignores the input which is then handled on the UI thread.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>