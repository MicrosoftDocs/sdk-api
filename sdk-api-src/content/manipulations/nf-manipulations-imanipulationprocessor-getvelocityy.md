---
UID: NF:manipulations.IManipulationProcessor.GetVelocityY
title: IManipulationProcessor::GetVelocityY
author: windows-sdk-content
description: Calculates and returns the vertical velocity.
old-location: wintouch\imanipulationprocessor_getvelocityy.htm
old-project: wintouch
ms.assetid: b531c4e5-8437-4869-9264-3fe131b8acc8
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetVelocityY, GetVelocityY method [Windows Touch], GetVelocityY method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetVelocityY method, IManipulationProcessor.GetVelocityY, IManipulationProcessor::GetVelocityY, manipulations/IManipulationProcessor::GetVelocityY, wintouch.imanipulationprocessor_getvelocityy
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
 - IManipulationProcessor.GetVelocityY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IManipulationProcessor::GetVelocityY


## -description


Calculates and returns the vertical velocity.


## -parameters




### -param velocityY






#### - pY [out]

The calculated vertical velocity.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.




## -remarks



This value is useful when you are using the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.




## -see-also




<a href="https://msdn.microsoft.com/64524f01-f7b2-4e78-97b8-20686018469f">GetVelocityX</a>



<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/3ba0aa0c-a819-4833-883b-218702052ce1">InitialVelocityY</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

