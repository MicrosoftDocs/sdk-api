---
UID: NF:manipulations.IManipulationProcessor.CompleteManipulation
title: IManipulationProcessor::CompleteManipulation
author: windows-sdk-content
description: The CompleteManipulation method is called when the developer chooses to end the manipulation.
old-location: wintouch\imanipulationprocessor_completemanipulation.htm
old-project: wintouch
ms.assetid: 01779628-1f46-4cea-90fa-1093e26e0285
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CompleteManipulation, CompleteManipulation method [Windows Touch], CompleteManipulation method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],CompleteManipulation method, IManipulationProcessor.CompleteManipulation, IManipulationProcessor::CompleteManipulation, manipulations/IManipulationProcessor::CompleteManipulation, wintouch.imanipulationprocessor_completemanipulation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations_i.c
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
 - IManipulationProcessor.CompleteManipulation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IManipulationProcessor::CompleteManipulation


## -description


The <b>CompleteManipulation</b> method is called when the developer chooses to end the manipulation. 


## -parameters






## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks




    This method raises the ManipulationCompleted() event in response.
  


  During a Windows Touch gesture, manipulation gets started as soon as first touch input is sent for processing. 
  If <b>CompleteManipulation</b> is called before the second touch input gets a chance to be processed, 
  the second touch input will start a new manipulation.  
  




## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

