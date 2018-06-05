---
UID: NF:manipulations._IManipulationEvents.ManipulationStarted
title: "_IManipulationEvents::ManipulationStarted"
author: windows-sdk-content
description: Handles the event for when manipulation or inertia begins.
old-location: wintouch\_imanipulationevents_manipulationstarted.htm
old-project: wintouch
ms.assetid: c3e63eb7-65e7-4394-89e4-d95d7e7877cf
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: ManipulationStarted, ManipulationStarted method [Windows Touch], ManipulationStarted method [Windows Touch],_IManipulationEvents interface, _IManipulationEvents interface [Windows Touch],ManipulationStarted method, _IManipulationEvents.ManipulationStarted, _IManipulationEvents::ManipulationStarted, manipulations/_IManipulationEvents::ManipulationStarted, wintouch._imanipulationevents_manipulationstarted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	manipulations.h
api_name:
-	_IManipulationEvents.ManipulationStarted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




    Manipulation events are generated for both the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> and <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> interfaces.
    If you are using the values from the <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure in calls to <a href="https://msdn.microsoft.com/2c192bc4-6922-4c70-961d-1f8684ad792b">ProcessDown</a>, the coordinates will be in 
    hundredths of a pixel.


#### Examples

The following code shows an implementation of the ManipulationStarted method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // place your code handler here to do any operations based on the manipulation

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
 

 

