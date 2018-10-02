---
UID: NN:winsatcominterfacei.IProvideWinSATAssessmentInfo
title: IProvideWinSATAssessmentInfo
author: windows-sdk-content
description: Gets summary information for a subcomponent of the assessment, for example, its score.
old-location: winsat\iprovidewinsatassessmentinfo.htm
tech.root: WinSAT
ms.assetid: 90036c75-6e9e-4d25-804b-02c423616de1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IProvideWinSATAssessmentInfo, IProvideWinSATAssessmentInfo interface [WinSAT], IProvideWinSATAssessmentInfo interface [WinSAT],described, winsat.iprovidewinsatassessmentinfo, winsatcominterfacei/IProvideWinSATAssessmentInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IProvideWinSATAssessmentInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

