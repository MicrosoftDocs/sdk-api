---
UID: NF:manipulations._IManipulationEvents.ManipulationCompleted
title: _IManipulationEvents::ManipulationCompleted (manipulations.h)
description: Handles the event when manipulation or inertia finishes.
helpviewer_keywords: ["ManipulationCompleted","ManipulationCompleted method [Windows Touch]","ManipulationCompleted method [Windows Touch]","_IManipulationEvents interface","_IManipulationEvents interface [Windows Touch]","ManipulationCompleted method","_IManipulationEvents.ManipulationCompleted","_IManipulationEvents::ManipulationCompleted","manipulations/_IManipulationEvents::ManipulationCompleted","wintouch._imanipulationevents_manipulationcompleted"]
old-location: wintouch\_imanipulationevents_manipulationcompleted.htm
tech.root: wintouch
ms.assetid: 1284df32-f4e8-43b3-b825-9172ad39f0e6
ms.date: 12/05/2018
ms.keywords: ManipulationCompleted, ManipulationCompleted method [Windows Touch], ManipulationCompleted method [Windows Touch],_IManipulationEvents interface, _IManipulationEvents interface [Windows Touch],ManipulationCompleted method, _IManipulationEvents.ManipulationCompleted, _IManipulationEvents::ManipulationCompleted, manipulations/_IManipulationEvents::ManipulationCompleted, wintouch._imanipulationevents_manipulationcompleted
req.header: manipulations.h
req.include-header: Manipulations.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - _IManipulationEvents::ManipulationCompleted
 - manipulations/_IManipulationEvents::ManipulationCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - _IManipulationEvents.ManipulationCompleted
---

# _IManipulationEvents::ManipulationCompleted


## -description

Handles the event when manipulation or inertia finishes.

## -parameters

### -param x [in]

The origin x-coordinate in user-defined coordinates.

### -param y [in]

The origin y-coordinate in user-defined coordinates.

### -param cumulativeTranslationX [in]

The total translation about the x-axis since the beginning of the manipulation in user-defined coordinates.

### -param cumulativeTranslationY [in]

The total translation about the y-axis since the beginning of the manipulation in user-defined coordinates.

### -param cumulativeScale [in]

The total scale change since the beginning of the manipulation as a percentage of the original size.

### -param cumulativeExpansion [in]

The total expansion change since the beginning of the manipulation in user-defined coordinates.

### -param cumulativeRotation [in]

The total rotation change since the beginning of the manipulation in radians.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code.

## -remarks

Manipulation events are generated for both the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> and <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> interfaces.
    If you are using the values from the <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structure in calls to <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup">ProcessUp</a>, the coordinates will be in 
    hundredths of a pixel.

<div class="alert"><b>Note</b>  When using inertia, calls to <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete">IInertiaProcessor::Complete</a> can force the current manipulation to be extrapolated resulting in large deltas being passed to the ManipulationCompleted event.
	 To address this issue, perform updates on the completed event in addition to the delta event.
	 </div>
<div> </div>

#### Examples

The following code shows an implementation of the ManipulationCompleted method.


```cpp



HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;
    m_fCumulativeTranslationX = cumulativeTranslationX;
    m_fCumulativeTranslationY = cumulativeTranslationY;
    m_fCumulativeScale = cumulativeScale;
    m_fCumulativeExpansion = cumulativeExpansion;
    m_fCumulativeRotation = cumulativeRotation;

    // Place your code handler here to do any operations based on the manipulation.

    return S_OK;
}
    
    
```

## -see-also

<a href="/windows/desktop/wintouch/adding-manipulation-support-in-unmanaged-code">Adding Manipulation Support to Unmanaged Code</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/wintouch/-imanipulationevents-methods">Methods</a>



<a href="/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents">_IManipulationEvents</a>