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

# IProvideWinSATResultsInfo::get_RatingStateDesc


## -description


<p class="CCE_Message">[IProvideWinSATResultsInfo::RatingStateDesc may be altered or unavailable for releases after Windows 8.1.]

Retrieves a string that you can use in a UI to indicate whether the assessment is valid.

This property is read-only.


## -parameters


## -remarks



If the assessment is valid, the string is "Windows Experience Index"; otherwise, the string is "Windows Experience Index : Unrated". To determine the validity of the assessment, call the <a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::get_AssessmentState</a> method.




## -see-also




<a href="https://msdn.microsoft.com/bd15bc63-a918-43a7-9864-4206a0b6af84">IProvideWinSATResultsInfo</a>



<a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::AssessmentState</a>
 

 

