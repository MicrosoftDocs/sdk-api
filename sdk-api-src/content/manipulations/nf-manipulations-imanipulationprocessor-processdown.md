---
UID: NF:manipulations.IManipulationProcessor.ProcessDown
title: IManipulationProcessor::ProcessDown
author: windows-sdk-content
description: The ProcessDown method feeds touch down data to the manipulation processor associated with a target.
old-location: wintouch\imanipulationprocessor_processdown.htm
tech.root: wintouch
ms.assetid: 2c192bc4-6922-4c70-961d-1f8684ad792b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessDown method, IManipulationProcessor.ProcessDown, IManipulationProcessor::ProcessDown, ProcessDown, ProcessDown method [Windows Touch], ProcessDown method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessDown, wintouch.imanipulationprocessor_processdown
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
 - IManipulationProcessor.ProcessDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::ProcessDown


## -description


The <b>ProcessDown</b> method feeds touch down data to the manipulation processor associated with a target.


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
    cases where performance is degrading you should use the <a href="https://msdn.microsoft.com/a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a">ProcessDownWithTime</a> method.




## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>
 

 

