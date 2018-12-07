---
UID: NF:manipulations.IManipulationProcessor.GetExpansionVelocity
title: IManipulationProcessor::GetExpansionVelocity
author: windows-sdk-content
description: The GetExpansionVelocity method calculates the rate that the target object is expanding at.
old-location: wintouch\imanipulationprocessor_getexpansionvelocity.htm
tech.root: wintouch
ms.assetid: 5dbaeaa3-4abf-485e-9f84-8450dce14fc9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetExpansionVelocity, GetExpansionVelocity method [Windows Touch], GetExpansionVelocity method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetExpansionVelocity method, IManipulationProcessor.GetExpansionVelocity, IManipulationProcessor::GetExpansionVelocity, manipulations/IManipulationProcessor::GetExpansionVelocity, wintouch.imanipulationprocessor_getexpansionvelocity
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IManipulationProcessor.GetExpansionVelocity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::GetExpansionVelocity


## -description


The <b>GetExpansionVelocity</b> method calculates the rate that the target object is expanding at.


## -parameters




### -param expansionVelocity [out]

The rate of expansion.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



This value is useful when you are using the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.




## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/c0e60b1c-98d0-4b50-ba5d-deda44debf56">InitialExpansionVelocity</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

