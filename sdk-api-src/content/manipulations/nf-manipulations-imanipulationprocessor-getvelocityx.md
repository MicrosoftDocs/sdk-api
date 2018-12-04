---
UID: NF:manipulations.IManipulationProcessor.GetVelocityX
title: IManipulationProcessor::GetVelocityX
author: windows-sdk-content
description: Calculates and returns the horizontal velocity for the target object.
old-location: wintouch\imanipulationprocessor_getvelocityx.htm
tech.root: wintouch
ms.assetid: 64524f01-f7b2-4e78-97b8-20686018469f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetVelocityX, GetVelocityX method [Windows Touch], GetVelocityX method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetVelocityX method, IManipulationProcessor.GetVelocityX, IManipulationProcessor::GetVelocityX, manipulations/IManipulationProcessor::GetVelocityX, wintouch.imanipulationprocessor_getvelocityx
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
 - IManipulationProcessor.GetVelocityX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::GetVelocityX


## -description


Calculates and returns the horizontal velocity for the target object.


## -parameters




### -param velocityX [out]

The calculated horizontal velocity.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.




## -remarks



This value is useful when you are using the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.




## -see-also




<a href="https://msdn.microsoft.com/b531c4e5-8437-4869-9264-3fe131b8acc8">GetVelocityY</a>



<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/23ae7083-0a78-4628-8a04-f9bd762aac02">InitialVelocityX</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

