---
UID: NF:winsatcominterfacei.IProvideWinSATAssessmentInfo.get_Score
title: IProvideWinSATAssessmentInfo::get_Score (winsatcominterfacei.h)
author: windows-sdk-content
description: Retrieves the score for the subcomponent.
old-location: winsat\iprovidewinsatassessmentinfo_score.htm
tech.root: WinSAT
ms.assetid: a1fbeb60-10dd-4082-8d2e-76c4baf35152
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IProvideWinSATAssessmentInfo interface [WinSAT],Score property, IProvideWinSATAssessmentInfo.Score, IProvideWinSATAssessmentInfo.get_Score, IProvideWinSATAssessmentInfo::Score, IProvideWinSATAssessmentInfo::get_Score, Score property [WinSAT], Score property [WinSAT],IProvideWinSATAssessmentInfo interface, get_Score, winsat.iprovidewinsatassessmentinfo_score, winsatcominterfacei/IProvideWinSATAssessmentInfo::Score, winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Score
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
 - IProvideWinSATAssessmentInfo.Score
 - IProvideWinSATAssessmentInfo.get_Score
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProvideWinSATAssessmentInfo::get_Score


## -description


<p class="CCE_Message">[IProvideWinSATAssessmentInfo::Score may be altered or unavailable for releases after Windows 8.1.]

Retrieves the score for the subcomponent.

This property is read-only.


## -parameters


## -remarks



The score represents the subcomponent's metrics as normalized by WinSAT.    The score is a floating point value that should be displayed with only one significant digit to the right of the decimal point.  The value is 0.0 if the assessment is unavailable or not valid. 

A user can use the score to determine if a subcomponent of the computer can support a specific type of application.  For example, a user that spends more time reading or writing documents may require a higher score for the disk than a user who runs scientific applications, and a user who runs scientific applications would probably want a higher CPU subcomponent score and may not be concerned with a lower disk score.

To get the base score for the computer, call the <a href="https://msdn.microsoft.com/4fe20830-bf86-4551-ba73-534740cabab5">IProvideWinSATResultsInfo::get_SystemRating</a> method. 


#### Examples

For an example, see the <a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/90036c75-6e9e-4d25-804b-02c423616de1">IProvideWinSATAssessmentInfo</a>



<a href="https://msdn.microsoft.com/adf4de42-9dfd-46a7-ae75-3bbcfd15dd68">Win32_WinSAT</a>
 

 

