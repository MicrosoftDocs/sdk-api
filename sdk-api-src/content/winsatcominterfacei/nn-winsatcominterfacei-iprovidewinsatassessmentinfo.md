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

# IProvideWinSATAssessmentInfo interface


## -description


<p class="CCE_Message">[IProvideWinSATAssessmentInfo may be altered or unavailable for releases after Windows 8.1.]

Gets summary information for a subcomponent of the assessment, for example, its score.

To get this interface, call the <a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.


## -remarks



To retrieve details of the subcomponent, call the <a href="https://msdn.microsoft.com/f8a1c664-bea3-4505-bcf0-2b8715dbe7dd">IQueryRecentWinSATAssessment::get_XML</a> method.




## -see-also




<a href="https://msdn.microsoft.com/bd15bc63-a918-43a7-9864-4206a0b6af84">IProvideWinSATResultsInfo</a>



<a href="https://msdn.microsoft.com/6849d8b6-d192-4520-a737-39e22e14a70f">IQueryRecentWinSATAssessment</a>
 

 

