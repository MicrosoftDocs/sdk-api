---
UID: NF:manipulations.IInertiaProcessor.get_InitialRadius
title: IInertiaProcessor::get_InitialRadius
author: windows-sdk-content
description: The InitialRadius property specifies the distance from the edge of the target to its center before the object was changed.
old-location: wintouch\iinertiaprocessor_initialradius.htm
old-project: wintouch
ms.assetid: 53179559-e65a-4b5b-b82a-f1fea0cb4509
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialRadius property, IInertiaProcessor.InitialRadius, IInertiaProcessor.get_InitialRadius, IInertiaProcessor::InitialRadius, IInertiaProcessor::get_InitialRadius, IInertiaProcessor::put_InitialRadius, InitialRadius property [Windows Touch], InitialRadius property [Windows Touch],IInertiaProcessor interface, get_InitialRadius, manipulations/IInertiaProcessor::InitialRadius, manipulations/IInertiaProcessor::get_InitialRadius, manipulations/IInertiaProcessor::put_InitialRadius, wintouch.iinertiaprocessor_initialradius
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
 - IInertiaProcessor.InitialRadius
 - IInertiaProcessor.get_InitialRadius
 - IInertiaProcessor.put_InitialRadius
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor::get_InitialRadius


## -description


The <b>InitialRadius</b> property specifies the distance from the edge of the target to its center before the object was changed.

This property is read/write.


## -parameters


## -remarks



If Inertia processing has already started, setting <b>InitialRadius</b> will reset the inertia engine to the initial state with new radius value applied.
	 

Call this function to set initial state of inertia. You would call this function most likely during the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event of the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>, or in the constructor of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/3261b461-add2-4e92-9a51-b2d46630fb4f">Handling Inertia in Unmanaged Code</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/188b6936-b36e-4e57-9118-8b61ed134c17">Inertia Mechanics</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>
 

 

