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

# tagHypothesisResult structure


## -description


The <b>HypothesisResult</b> structure contains information about a hypothesis returned from a helper class. The hypothesis is obtained via a call to <a href="https://msdn.microsoft.com/d17f5241-6efb-45a7-b355-8343e48b3261">GetLowerHypotheses</a>.


## -struct-fields




### -field hypothesis

Type: <b><a href="https://msdn.microsoft.com/8f137633-8501-404c-9540-d558be9beeca">HYPOTHESIS</a></b>

Information for a specific hypothesis.


### -field pathStatus

Type: <b><a href="https://msdn.microsoft.com/2ad72ac5-3f33-4206-be39-1cfe11ee840d">DIAGNOSIS_STATUS</a></b>

The status of the child helper class and its children. 

If the hypothesis or any of its children indicated <b>DS_CONFIRMED</b> in a call to <a href="https://msdn.microsoft.com/623de90f-c2dc-4879-9baf-4051d2d3691c">LowHealth</a>, then this value will be <b>DS_CONFIRMED</b>. If no problems exist in such a call, the value will be <b>DS_REJECTED</b>. The value will be <b>DS_INDETERMINATE</b> if the health of the component is not clear.


## -see-also




<a href="https://msdn.microsoft.com/2ad72ac5-3f33-4206-be39-1cfe11ee840d">DIAGNOSIS_STATUS</a>



<a href="https://msdn.microsoft.com/d17f5241-6efb-45a7-b355-8343e48b3261">GetLowerHypotheses</a>



<a href="https://msdn.microsoft.com/8f137633-8501-404c-9540-d558be9beeca">HYPOTHESIS</a>



<a href="https://msdn.microsoft.com/623de90f-c2dc-4879-9baf-4051d2d3691c">LowHealth</a>
 

 

