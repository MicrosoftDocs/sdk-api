---
UID: NF:manipulations.IInertiaProcessor.get_InitialVelocityX
title: IInertiaProcessor::get_InitialVelocityX
author: windows-sdk-content
description: The InitialVelocityX property specifies the initial movement of the target object on the horizontal axis.
old-location: wintouch\iinertiaprocessor_initialvelocityx.htm
old-project: wintouch
ms.assetid: 23ae7083-0a78-4628-8a04-f9bd762aac02
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialVelocityX property, IInertiaProcessor.InitialVelocityX, IInertiaProcessor.get_InitialVelocityX, IInertiaProcessor::InitialVelocityX, IInertiaProcessor::get_InitialVelocityX, IInertiaProcessor::put_InitialVelocityX, InitialVelocityX property [Windows Touch], InitialVelocityX property [Windows Touch],IInertiaProcessor interface, get_InitialVelocityX, manipulations/IInertiaProcessor::InitialVelocityX, manipulations/IInertiaProcessor::get_InitialVelocityX, manipulations/IInertiaProcessor::put_InitialVelocityX, wintouch.iinertiaprocessor_initialvelocityx
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
-	IInertiaProcessor.InitialVelocityX
-	IInertiaProcessor.get_InitialVelocityX
-	IInertiaProcessor.put_InitialVelocityX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor::get_InitialVelocityX


## -description


The <b>InitialVelocityX</b> property specifies the initial movement of the target object on the horizontal axis.

This property is read/write.


## -parameters


## -remarks




      If Inertia processing has already started, setting <b>InitialVelocityX</b> will reset the inertia engine to the initial state with new velocity values applied.	 		
	 

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/64524f01-f7b2-4e78-97b8-20686018469f">GetVelocityX</a>



<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/3ba0aa0c-a819-4833-883b-218702052ce1">InitialVelocityY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>
 

 

