---
UID: NF:manipulations.IInertiaProcessor.get_InitialAngularVelocity
title: IInertiaProcessor::get_InitialAngularVelocity (manipulations.h)
author: windows-sdk-content
description: The InitialAngularVelocity property specifies the rotational (angular) velocity of the target when movement begins.
old-location: wintouch\iinertiaprocessor_initialangularvelocity.htm
tech.root: wintouch
ms.assetid: a15ac600-ef03-4234-ac38-dc3cf212a3cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialAngularVelocity property, IInertiaProcessor.InitialAngularVelocity, IInertiaProcessor.get_InitialAngularVelocity, IInertiaProcessor::InitialAngularVelocity, IInertiaProcessor::get_InitialAngularVelocity, IInertiaProcessor::put_InitialAngularVelocity, InitialAngularVelocity property [Windows Touch], InitialAngularVelocity property [Windows Touch],IInertiaProcessor interface, get_InitialAngularVelocity, manipulations/IInertiaProcessor::InitialAngularVelocity, manipulations/IInertiaProcessor::get_InitialAngularVelocity, manipulations/IInertiaProcessor::put_InitialAngularVelocity, wintouch.iinertiaprocessor_initialangularvelocity
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
 - IInertiaProcessor.InitialAngularVelocity
 - IInertiaProcessor.get_InitialAngularVelocity
 - IInertiaProcessor.put_InitialAngularVelocity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInertiaProcessor::get_InitialAngularVelocity


## -description


The <b>InitialAngularVelocity</b> property specifies the rotational (angular) velocity of the target when movement begins.

This property is read/write.


## -parameters


## -remarks




<a href="https://msdn.microsoft.com/42fcda66-8992-4a44-b4d5-04d4f2c7e25a">DesiredRotation</a> and <a href="https://msdn.microsoft.com/ee3bb3c8-4d7d-424b-abc9-db7307793794">DesiredAngularDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.  If the <b>DesiredRotation</b> property is set, the API will set the <b>DesiredAngularDeceleration</b> property so that the object will stop after the desired number of radians.
       The unit of angular accelleration is radians.
      

If inertia processing has already started, setting <b>InitialAngularVelocity</b> will reset the inertia engine to the initial state with new velocity values applied.
		

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/42fcda66-8992-4a44-b4d5-04d4f2c7e25a">DesiredRotation</a>



<a href="https://msdn.microsoft.com/3253837f-c5ea-47f7-ba0a-86e0ed4e228e">GetAngularVelocity</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/c0e60b1c-98d0-4b50-ba5d-deda44debf56">InitialExpansionVelocity</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

