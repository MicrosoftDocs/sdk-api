---
UID: NF:manipulations.IManipulationProcessor.ProcessMove
title: IManipulationProcessor::ProcessMove
author: windows-sdk-content
description: The ProcessMove method feeds movement data for the target object to its manipulation processor.
old-location: wintouch\imanipulationprocessor_processmove.htm
old-project: wintouch
ms.assetid: e2c0e975-3edd-43d5-8a58-2d8166413c76
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessMove method, IManipulationProcessor.ProcessMove, IManipulationProcessor::ProcessMove, ProcessMove, ProcessMove method [Windows Touch], ProcessMove method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessMove, wintouch.imanipulationprocessor_processmove
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	manipulations.h
api_name:
-	IManipulationProcessor.ProcessMove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IManipulationProcessor::ProcessMove


## -description


The <b>ProcessMove</b> method feeds movement data for the target object to its manipulation processor.


## -parameters




### -param manipulatorId

The identifier for the touch contact that you want to process.


### -param x

The horizontal coordinate data associated with the target.


### -param y

The vertical coordinate data associated with the target.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks




    This method takes a timestamp using system time rather than from the touch hardware. To improve the experience in 
    cases where performance is degrading you should use the <a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a> method.    




## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>



<a href="https://msdn.microsoft.com/2c192bc4-6922-4c70-961d-1f8684ad792b">ProcessDown</a>



<a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a>



<a href="https://msdn.microsoft.com/c93f6729-5e50-41a1-867c-93e4ce9ecda9">ProcessUp</a>
 

 

