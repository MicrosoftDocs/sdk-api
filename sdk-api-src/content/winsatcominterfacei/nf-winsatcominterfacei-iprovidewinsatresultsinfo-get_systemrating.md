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

# IProvideWinSATResultsInfo::get_SystemRating


## -description


<p class="CCE_Message">[IProvideWinSATResultsInfo::SystemRating may be altered or unavailable for releases after Windows 8.1.]

Retrieves the base score for the computer.

This property is read-only.


## -parameters


## -remarks



The Windows Experience Index feature measures the capability of your computer's hardware configuration and expresses this measurement as a number called a base score. A higher base score generally means that your computer will perform better and faster than a computer with a lower base score, especially when performing more advanced and resource-intensive tasks. 



Each hardware component receives an individual subscore. Your computer's base score is determined by the lowest subscore. For example, if the lowest subscore of an individual hardware component is 2.6, then the base score is 2.6. The base score is not an average of the combined subscores.



You can use the base score to confidently buy programs and other software that are matched to your computer's base score. For example, if your computer has a base score of 3.3, then you can confidently purchase any software designed for this version of Windows that requires a computer with a base score of 3 or lower.


To get the score for a subcomponent of the assessment, such as the CPU, call the <a href="https://msdn.microsoft.com/a1fbeb60-10dd-4082-8d2e-76c4baf35152">IProvideWinSATAssessmentInfo::get_Score</a> method.


#### Examples

For an example, see the <a href="https://msdn.microsoft.com/11697416-aa4d-4724-bd63-8d123e2b32cb">IQueryRecentWinSATAssessment::Info</a> property.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bd15bc63-a918-43a7-9864-4206a0b6af84">IProvideWinSATResultsInfo</a>



<a href="https://msdn.microsoft.com/adf4de42-9dfd-46a7-ae75-3bbcfd15dd68">Win32_WinSAT</a>
 

 

