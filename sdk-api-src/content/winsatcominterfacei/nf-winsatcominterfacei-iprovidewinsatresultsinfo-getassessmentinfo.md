---
UID: NF:winsatcominterfacei.IProvideWinSATResultsInfo.GetAssessmentInfo
title: IProvideWinSATResultsInfo::GetAssessmentInfo
author: windows-sdk-content
description: Retrieves summary information for a subcomponent of the assessment.
old-location: winsat\iprovidewinsatresultsinfo_getassessmentinfo.htm
tech.root: WinSAT
ms.assetid: dfa4d740-2dfd-41b5-a0be-a241f9ece939
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetAssessmentInfo, GetAssessmentInfo method [WinSAT], GetAssessmentInfo method [WinSAT],IProvideWinSATResultsInfo interface, IProvideWinSATResultsInfo interface [WinSAT],GetAssessmentInfo method, IProvideWinSATResultsInfo.GetAssessmentInfo, IProvideWinSATResultsInfo::GetAssessmentInfo, winsat.iprovidewinsatresultsinfo_getassessmentinfo, winsatcominterfacei/IProvideWinSATResultsInfo::GetAssessmentInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Winsatapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IProvideWinSATResultsInfo.GetAssessmentInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsatcominterfacei.h
: 
- IProvideWinSATResultsInfo.GetAssessmentInfo
: 
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
 

 

