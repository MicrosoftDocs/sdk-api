---
UID: NF:manipulations.IManipulationProcessor.GetAngularVelocity
title: IManipulationProcessor::GetAngularVelocity
author: windows-driver-content
description: The GetAngularVelocity method calculates the rotational velocity that the target object is moving at.
old-location: wintouch\imanipulationprocessor_getangularvelocity.htm
old-project: wintouch
ms.assetid: 3253837f-c5ea-47f7-ba0a-86e0ed4e228e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetAngularVelocity, GetAngularVelocity method [Windows Touch], GetAngularVelocity method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetAngularVelocity method, IManipulationProcessor.GetAngularVelocity, IManipulationProcessor::GetAngularVelocity, manipulations/IManipulationProcessor::GetAngularVelocity, wintouch.imanipulationprocessor_getangularvelocity
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
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	manipulations.h
api_name:
-	IManipulationProcessor.GetAngularVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IManipulationProcessor::GetAngularVelocity


## -description


The <b>GetAngularVelocity</b> method calculates the rotational velocity that the target object is moving at.


## -parameters




### -param angularVelocity






#### - pAngularVelocity [out]

The calculated rotational velocity.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



This value is useful when you are setting up the initial state of the <a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.

This property is expressed in radians per millisecond if explicit timestamps are not specified by using calls to <a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a>, <b>ProcessMoveWithTime</b>, and <a href="https://msdn.microsoft.com/fafea353-9126-454d-9311-4859e5ae5712">ProcessUpWithTime</a>. Otherwise, this function uses radians per user defined time units.




## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/a15ac600-ef03-4234-ac38-dc3cf212a3cb">InitialAngularVelocity</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

