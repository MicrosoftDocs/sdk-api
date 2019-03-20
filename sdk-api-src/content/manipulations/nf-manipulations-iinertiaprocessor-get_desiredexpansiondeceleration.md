---
UID: NF:manipulations.IInertiaProcessor.get_DesiredExpansionDeceleration
title: IInertiaProcessor::get_DesiredExpansionDeceleration (manipulations.h)
author: windows-sdk-content
description: The DesiredExpansionDeceleration property specifies the rate at which the object will stop expanding.
old-location: wintouch\iinertiaprocessor_desiredexpansiondeceleration.htm
tech.root: wintouch
ms.assetid: b21d9aa8-0c86-45fe-9573-023929cf7faa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DesiredExpansionDeceleration property [Windows Touch], DesiredExpansionDeceleration property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredExpansionDeceleration property, IInertiaProcessor.DesiredExpansionDeceleration, IInertiaProcessor.get_DesiredExpansionDeceleration, IInertiaProcessor::DesiredExpansionDeceleration, IInertiaProcessor::get_DesiredExpansionDeceleration, IInertiaProcessor::put_DesiredExpansionDeceleration, get_DesiredExpansionDeceleration, manipulations/IInertiaProcessor::DesiredExpansionDeceleration, manipulations/IInertiaProcessor::get_DesiredExpansionDeceleration, manipulations/IInertiaProcessor::put_DesiredExpansionDeceleration, wintouch.iinertiaprocessor_desiredexpansiondeceleration
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IInertiaProcessor.DesiredExpansionDeceleration
 - IInertiaProcessor.get_DesiredExpansionDeceleration
 - IInertiaProcessor.put_DesiredExpansionDeceleration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInertiaProcessor::get_DesiredExpansionDeceleration


## -description


The <b>DesiredExpansionDeceleration</b> property specifies the rate at which the object will stop expanding.

This property is read/write.


## -parameters


## -remarks



<b>DesiredExpansionDeceleration</b> and <a href="https://msdn.microsoft.com/1d686bb1-a00b-43fc-804b-5a1d8bb69499">DesiredExpansion</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredExpansionDeceleration</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d686bb1-a00b-43fc-804b-5a1d8bb69499">DesiredExpansion</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/c0e60b1c-98d0-4b50-ba5d-deda44debf56">InitialExpansionVelocity</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

