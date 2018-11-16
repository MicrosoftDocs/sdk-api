---
UID: NF:manipulations.IInertiaProcessor.get_DesiredRotation
title: IInertiaProcessor::get_DesiredRotation
author: windows-sdk-content
description: The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians.
old-location: wintouch\iinertiaprocessor_desiredrotation.htm
tech.root: wintouch
ms.assetid: 42fcda66-8992-4a44-b4d5-04d4f2c7e25a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DesiredRotation property [Windows Touch], DesiredRotation property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredRotation property, IInertiaProcessor.DesiredRotation, IInertiaProcessor.get_DesiredRotation, IInertiaProcessor::DesiredRotation, IInertiaProcessor::get_DesiredRotation, IInertiaProcessor::put_DesiredRotation, get_DesiredRotation, manipulations/IInertiaProcessor::DesiredRotation, manipulations/IInertiaProcessor::get_DesiredRotation, manipulations/IInertiaProcessor::put_DesiredRotation, wintouch.iinertiaprocessor_desiredrotation
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInertiaProcessor.DesiredRotation
 - IInertiaProcessor.get_DesiredRotation
 - IInertiaProcessor.put_DesiredRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- manipulations.h
: 
- IInertiaProcessor.get_DesiredRotation
: 
---

# IInertiaProcessor::get_DesiredRotation


## -description


The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians.

This property is read/write.


## -parameters


## -remarks



<b>DesiredRotation</b> and <a href="https://msdn.microsoft.com/ee3bb3c8-4d7d-424b-abc9-db7307793794">DesiredAngularDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredRotation</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/ee3bb3c8-4d7d-424b-abc9-db7307793794">DesiredAngularDeceleration</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/a15ac600-ef03-4234-ac38-dc3cf212a3cb">InitialAngularVelocity</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

