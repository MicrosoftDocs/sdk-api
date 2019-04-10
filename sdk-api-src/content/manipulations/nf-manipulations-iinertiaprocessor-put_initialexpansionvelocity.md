---
UID: NF:manipulations.IInertiaProcessor.put_InitialExpansionVelocity
title: IInertiaProcessor::put_InitialExpansionVelocity (manipulations.h)
author: windows-sdk-content
description: The InitialExpansionVelocity property specifies the rate of radius expansion for a target when the target was affected by inertia.
old-location: wintouch\iinertiaprocessor_initialexpansionvelocity.htm
tech.root: wintouch
ms.assetid: c0e60b1c-98d0-4b50-ba5d-deda44debf56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialExpansionVelocity property, IInertiaProcessor.InitialExpansionVelocity, IInertiaProcessor.put_InitialExpansionVelocity, IInertiaProcessor::InitialExpansionVelocity, IInertiaProcessor::get_InitialExpansionVelocity, IInertiaProcessor::put_InitialExpansionVelocity, InitialExpansionVelocity property [Windows Touch], InitialExpansionVelocity property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialExpansionVelocity, manipulations/IInertiaProcessor::get_InitialExpansionVelocity, manipulations/IInertiaProcessor::put_InitialExpansionVelocity, put_InitialExpansionVelocity, wintouch.iinertiaprocessor_initialexpansionvelocity
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
 - IInertiaProcessor.InitialExpansionVelocity
 - IInertiaProcessor.get_InitialExpansionVelocity
 - IInertiaProcessor.put_InitialExpansionVelocity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInertiaProcessor::put_InitialExpansionVelocity


## -description


The <b>InitialExpansionVelocity</b> property specifies the rate of radius expansion for a target when the target was affected by inertia.

This property is read/write.


## -parameters


## -remarks



The amount of expansion that the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> exatrapolates will be detemined by the <a href="https://msdn.microsoft.com/1d686bb1-a00b-43fc-804b-5a1d8bb69499">DesiredExpansion</a> or <a href="https://msdn.microsoft.com/b21d9aa8-0c86-45fe-9573-023929cf7faa">DesiredExpansionDeceleration</a> property.
      <b>DesiredExpansion</b> and <b>DesiredExpansionDeceleration</b> are mutually exclusive.  If one is set, the other should be NaN.
    If using the <b>DesiredExpansion</b> property, the API will set the appropriate <b>DesiredExpansionDeceleration</b> value to expand the requested amount.

If inertia processing has already started, setting <b>InitialExpansionVelocity</b> will reset the inertia engine to the initial state with new velocity values applied.

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d686bb1-a00b-43fc-804b-5a1d8bb69499">DesiredExpansion</a>



<a href="https://msdn.microsoft.com/b21d9aa8-0c86-45fe-9573-023929cf7faa">DesiredExpansionDeceleration</a>



<a href="https://msdn.microsoft.com/5dbaeaa3-4abf-485e-9f84-8450dce14fc9">GetExpansionVelocity</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

