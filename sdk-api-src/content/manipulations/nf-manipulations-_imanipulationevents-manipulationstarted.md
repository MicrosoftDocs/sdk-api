---
UID: NF:manipulations._IManipulationEvents.ManipulationStarted
title: _IManipulationEvents::ManipulationStarted (manipulations.h)
description: Handles the event for when manipulation or inertia begins.
helpviewer_keywords: ["ManipulationStarted","ManipulationStarted method [Windows Touch]","ManipulationStarted method [Windows Touch]","_IManipulationEvents interface","_IManipulationEvents interface [Windows Touch]","ManipulationStarted method","_IManipulationEvents.ManipulationStarted","_IManipulationEvents::ManipulationStarted","manipulations/_IManipulationEvents::ManipulationStarted","wintouch._imanipulationevents_manipulationstarted"]
old-location: wintouch\_imanipulationevents_manipulationstarted.htm
tech.root: wintouch
ms.assetid: c3e63eb7-65e7-4394-89e4-d95d7e7877cf
ms.date: 12/05/2018
ms.keywords: ManipulationStarted, ManipulationStarted method [Windows Touch], ManipulationStarted method [Windows Touch],_IManipulationEvents interface, _IManipulationEvents interface [Windows Touch],ManipulationStarted method, _IManipulationEvents.ManipulationStarted, _IManipulationEvents::ManipulationStarted, manipulations/_IManipulationEvents::ManipulationStarted, wintouch._imanipulationevents_manipulationstarted
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
 - _IManipulationEvents::ManipulationStarted
 - manipulations/_IManipulationEvents::ManipulationStarted
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
 - _IManipulationEvents.ManipulationStarted
---

# _IManipulationEvents::ManipulationStarted


## -description

Handles the event for when manipulation or inertia begins.

## -parameters

### -param x [in]

The origin x-coordinate in user-defined coordinates.

### -param y [in]

The origin y-coordinate in user-defined coordinates.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code.

## -remarks

Manipulation events are generated for both the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> and <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> interfaces.
    If you are using the values from the <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structure in calls to <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown">ProcessDown</a>, the coordinates will be in 
    hundredths of a pixel.


#### Examples

The following code shows an implementation of the ManipulationStarted method.


```cpp

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // place your code handler here to do any operations based on the manipulation

    return S_OK;
}
    
    
```

## -see-also

<a href="/windows/desktop/wintouch/adding-manipulation-support-in-unmanaged-code">Adding Manipulation Support to Unmanaged Code</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/wintouch/-imanipulationevents-methods">Methods</a>



<a href="/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents">_IManipulationEvents</a>