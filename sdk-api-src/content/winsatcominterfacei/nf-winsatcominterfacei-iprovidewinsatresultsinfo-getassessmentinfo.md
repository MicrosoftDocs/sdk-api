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

# IProvideWinSATResultsInfo::GetAssessmentInfo


## -description


<p class="CCE_Message">[IProvideWinSATResultsInfo::GetAssessmentInfo may be altered or unavailable for releases after Windows 8.1.]

Retrieves summary information for a subcomponent of the assessment.


## -parameters




### -param assessment [in]

A subcomponent of the assessment whose summary information you want to retrieve. For possible values, see the <a href="https://msdn.microsoft.com/7e54df13-4415-42b8-b140-e35ea440ef68">WINSAT_ASSESSMENT_TYPE</a> enumeration.


### -param ppinfo [out]

An <a href="https://msdn.microsoft.com/90036c75-6e9e-4d25-804b-02c423616de1">IProvideWinSATAssessmentInfo</a> interface that you use to get the score for the subcomponent.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/bd15bc63-a918-43a7-9864-4206a0b6af84">IProvideWinSATResultsInfo</a>
 

 

