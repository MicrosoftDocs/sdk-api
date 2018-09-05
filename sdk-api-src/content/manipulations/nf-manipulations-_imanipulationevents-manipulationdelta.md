---
UID: NF:manipulations._IManipulationEvents.ManipulationDelta
title: "_IManipulationEvents::ManipulationDelta"
author: windows-sdk-content
description: Handles events that happen when a manipulated object changes.
old-location: wintouch\_imanipulationevents_manipulationdelta.htm
old-project: wintouch
ms.assetid: bebac896-c48d-4e6e-98ce-4b7d1dec101c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ManipulationDelta, ManipulationDelta method [Windows Touch], ManipulationDelta method [Windows Touch],_IManipulationEvents interface, _IManipulationEvents interface [Windows Touch],ManipulationDelta method, _IManipulationEvents.ManipulationDelta, _IManipulationEvents::ManipulationDelta, manipulations/_IManipulationEvents::ManipulationDelta, wintouch._imanipulationevents_manipulationdelta
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations.h
req.redist: 
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
tech.root: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - _IManipulationEvents.ManipulationDelta
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _IManipulationEvents::ManipulationDelta


## -description


Handles events that happen when a manipulated object changes.


## -parameters




### -param x [in]

The origin x-coordinate in user-defined coordinates.


### -param y [in]

The origin y-coordinate in user-defined coordinates.


### -param translationDeltaX [in]

The translation change about the x-axis in user-defined coordinates since the last event.


### -param translationDeltaY [in]

The translation change about the y-axis in user-defined coordinates since the last event.


### -param scaleDelta [in]

The scale change since the previous event as a percentage of the previous scale.


### -param expansionDelta [in]

The expansion change since the previous event in user-defined coordinates.


### -param rotationDelta [in]

The rotation change since the previous event in radians.


### -param cumulativeTranslationX [in]

The translation about the x-axis since the beginning of the manipulation in user-defined coordinates.


### -param cumulativeTranslationY [in]

The translation about the y-axis since the beginning of the manipulation in user-defined coordinates.


### -param cumulativeScale [in]

The scale change since the beginning of the manipulation as a percentage of the original size.


### -param cumulativeExpansion [in]

The expansion change since the beginning of the manipulation in user-defined coordinates.


### -param cumulativeRotation [in]

The rotation change since the beginning of the manipulation in radians.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code.




## -remarks



Manipulation events are generated for both the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> and <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> interfaces.
    If you are using the values from the <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure in calls to <a href="https://msdn.microsoft.com/e2c0e975-3edd-43d5-8a58-2d8166413c76">ProcessMove</a>, the coordinates will be in 
    hundredths of a pixel.

<div class="alert"><b>Note</b>  When using inertia, calls to <a href="https://msdn.microsoft.com/ff41789c-afc5-419b-9767-e99572b9b41e">IInertiaProcessor::Complete</a>can force the current manipulation to be extrapolated resulting in large deltas being passed to the ManipulationCompleted event.
	 To address this issue, perform updates on the completed event in addition to the delta event.
	 </div>
<div> </div>

#### Examples

The following code shows an implementation of the ManipulationDelta method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;

    // Place your code handler here to do any operations based on the manipulation.

    return S_OK;
}    
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7d8c6230-eaca-43c7-ad2f-651851b69d7f">Adding Manipulation Support to Unmanaged Code</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/ac697a9b-3cef-4100-8ad3-aaa867b94ec4">Methods</a>



<a href="https://msdn.microsoft.com/be392a13-3165-44ff-bcd6-ed0075c669c4">_IManipulationEvents</a>
 

 

