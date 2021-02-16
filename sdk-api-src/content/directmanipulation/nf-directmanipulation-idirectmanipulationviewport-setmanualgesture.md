---
UID: NF:directmanipulation.IDirectManipulationViewport.SetManualGesture
title: IDirectManipulationViewport::SetManualGesture (directmanipulation.h)
description: Sets which gestures are ignored by Direct Manipulation.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetManualGesture method","IDirectManipulationViewport.SetManualGesture","IDirectManipulationViewport::SetManualGesture","SetManualGesture","SetManualGesture method [Direct Manipulation]","SetManualGesture method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setmanualgesture","directmanipulation/IDirectManipulationViewport::SetManualGesture"]
old-location: directmanipulation\idirectmanipulationviewport_setmanualgesture.htm
tech.root: directmanipulation
ms.assetid: EBBBCEDB-8BAC-4E87-A69C-9730865A257F
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetManualGesture method, IDirectManipulationViewport.SetManualGesture, IDirectManipulationViewport::SetManualGesture, SetManualGesture, SetManualGesture method [Direct Manipulation], SetManualGesture method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setmanualgesture, directmanipulation/IDirectManipulationViewport::SetManualGesture
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
 - IDirectManipulationViewport::SetManualGesture
 - directmanipulation/IDirectManipulationViewport::SetManualGesture
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
 - IDirectManipulationViewport.SetManualGesture
---

# IDirectManipulationViewport::SetManualGesture


## -description

Sets which gestures are ignored by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

## -parameters

### -param configuration [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_gesture_configuration">DIRECTMANIPULATION_GESTURE_CONFIGURATION</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use this method to specify which gestures the application processes on the UI thread. If a gesture is recognized, it will be passed to the application for processing and ignored by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.


#### Examples

The following example shows how zoom gestures can be ignored by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> and handled by the application, which may have custom zoom behavior implementation.


```
HRESULT hr = pViewport->SetManualGesture(DIRECTMANIPULATION_GESTURE_PINCH_ZOOM);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>