---
UID: NF:manipulations.IInertiaProcessor.get_InitialOriginY
title: IInertiaProcessor::get_InitialOriginY
author: windows-sdk-content
description: The InitialOriginY property specifies the starting vertical location for a target with inertia.
old-location: wintouch\iinertiaprocessor_initialoriginy.htm
old-project: wintouch
ms.assetid: 4b817f8b-79e9-4409-a6b2-2096759bab59
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialOriginY property, IInertiaProcessor.InitialOriginY, IInertiaProcessor.get_InitialOriginY, IInertiaProcessor::InitialOriginY, IInertiaProcessor::get_InitialOriginY, IInertiaProcessor::put_InitialOriginY, InitialOriginY property [Windows Touch], InitialOriginY property [Windows Touch],IInertiaProcessor interface, get_InitialOriginY, manipulations/IInertiaProcessor::InitialOriginY, manipulations/IInertiaProcessor::get_InitialOriginY, manipulations/IInertiaProcessor::put_InitialOriginY, wintouch.iinertiaprocessor_initialoriginy
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
 - IInertiaProcessor.InitialOriginY
 - IInertiaProcessor.get_InitialOriginY
 - IInertiaProcessor.put_InitialOriginY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor::get_InitialOriginY


## -description


The <b>InitialOriginY</b> property specifies the starting vertical location for a target with inertia.

This property is read/write.


## -parameters


## -remarks



A user can manipulate an object to set the <b>InitialOriginY</b> to be outside of the elastic bounds.
	 Setting <b>InitialOriginY</b> to a value outside of the elastic bounds will cause an exception to be thrown.
	 To prevent  users from setting the origin out of bounds, check that <b>InitialOriginY</b> is valid before setting it 
	 on an <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.	 If Inertia processing has already started, calling put_InitialOriginY() 
	 will reset the inertia state to initial time stamp.
	 

All locations used for the inertia and manipulation processor are relative. If you want to use screen coordinates, 
		  you pass screen coordinates to the manipulation (or inertia) processor; if you want to use absolute coordinates, you 
		  pass those into the processor you are using. 	 
	 

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/4b817f8b-79e9-4409-a6b2-2096759bab59">InitialOriginY</a>



<a href="https://msdn.microsoft.com/47fd1a49-8e14-4076-8ce6-f0c4917e8cf1">Properties</a>
 

 

