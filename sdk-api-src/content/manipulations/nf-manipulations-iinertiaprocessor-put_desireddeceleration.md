---
UID: NF:manipulations.IInertiaProcessor.put_DesiredDeceleration
title: IInertiaProcessor::put_DesiredDeceleration (manipulations.h)
author: windows-sdk-content
description: The DesiredDeceleration property specifies the desired rate at which translation operations will decelerate.
old-location: wintouch\iinertiaprocessor_desireddeceleration.htm
tech.root: wintouch
ms.assetid: 2ad39e7e-b433-4a40-aea2-53cf23247f25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DesiredDeceleration property [Windows Touch], DesiredDeceleration property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredDeceleration property, IInertiaProcessor.DesiredDeceleration, IInertiaProcessor.put_DesiredDeceleration, IInertiaProcessor::DesiredDeceleration, IInertiaProcessor::get_DesiredDeceleration, IInertiaProcessor::put_DesiredDeceleration, manipulations/IInertiaProcessor::DesiredDeceleration, manipulations/IInertiaProcessor::get_DesiredDeceleration, manipulations/IInertiaProcessor::put_DesiredDeceleration, put_DesiredDeceleration, wintouch.iinertiaprocessor_desireddeceleration
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
 - IInertiaProcessor.DesiredDeceleration
 - IInertiaProcessor.get_DesiredDeceleration
 - IInertiaProcessor.put_DesiredDeceleration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInertiaProcessor::put_DesiredDeceleration


## -description


The <b>DesiredDeceleration</b> property specifies the desired rate at which translation operations will decelerate.

This property is read/write.


## -parameters


## -remarks



<b>DesiredDeceleration</b> and <a href="https://msdn.microsoft.com/cbcd7ce7-7df4-48d8-acfe-dc206f5d70d1">DesiredDisplacement</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredDeceleration</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/cbcd7ce7-7df4-48d8-acfe-dc206f5d70d1">DesiredDisplacement</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/23ae7083-0a78-4628-8a04-f9bd762aac02">InitialVelocityX</a>



<a href="https://msdn.microsoft.com/3ba0aa0c-a819-4833-883b-218702052ce1">InitialVelocityY</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

