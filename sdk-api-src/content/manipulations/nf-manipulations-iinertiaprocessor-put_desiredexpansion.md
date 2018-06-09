---
UID: NF:manipulations.IInertiaProcessor.put_DesiredExpansion
title: IInertiaProcessor::put_DesiredExpansion
author: windows-sdk-content
description: The DesiredExpansion property specifies the desired change in the object's average radius.
old-location: wintouch\iinertiaprocessor_desiredexpansion.htm
old-project: wintouch
ms.assetid: 1d686bb1-a00b-43fc-804b-5a1d8bb69499
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DesiredExpansion property [Windows Touch], DesiredExpansion property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredExpansion property, IInertiaProcessor.DesiredExpansion, IInertiaProcessor.put_DesiredExpansion, IInertiaProcessor::DesiredExpansion, IInertiaProcessor::get_DesiredExpansion, IInertiaProcessor::put_DesiredExpansion, manipulations/IInertiaProcessor::DesiredExpansion, manipulations/IInertiaProcessor::get_DesiredExpansion, manipulations/IInertiaProcessor::put_DesiredExpansion, put_DesiredExpansion, wintouch.iinertiaprocessor_desiredexpansion
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IInertiaProcessor.DesiredExpansion
 - IInertiaProcessor.get_DesiredExpansion
 - IInertiaProcessor.put_DesiredExpansion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor::put_DesiredExpansion


## -description


The <b>DesiredExpansion</b> property specifies the desired change in the object's average radius.

This property is read/write.


## -parameters


## -remarks



<b>DesiredExpansion</b> and <a href="https://msdn.microsoft.com/b21d9aa8-0c86-45fe-9573-023929cf7faa">DesiredExpansionDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.


        If inertia processing has already started, setting <b>DesiredExpansion</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/b21d9aa8-0c86-45fe-9573-023929cf7faa">DesiredExpansionDeceleration</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/c0e60b1c-98d0-4b50-ba5d-deda44debf56">InitialExpansionVelocity</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>
 

 

