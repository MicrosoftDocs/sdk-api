---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IReferenceTrackerTarget::xaml


## -description


Indicates that the reference tracker is returning the target XAML object(s) from previous calls to  <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">FindTrackerTargets</a>.  Note that the reference is held by the reference tracker object in lieu of <b>IUnknown::AddRef</b>.


## -parameters






## -remarks



  When the XAML framework keeps this reference in lieu of a COM reference, it indicates that the framework must call your implementation of <a href="https://msdn.microsoft.com/2750e8b1-eeeb-411a-89a8-b63b26f731ac">Peg</a> to ensure that the target does not get collected.




## -see-also




<a href="https://msdn.microsoft.com/204c647d-65c0-4b0e-b0fa-1abe9e8fdedd">IReferenceTrackerTarget</a>
 

 

