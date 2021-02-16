---
UID: NF:winsatcominterfacei.IProvideWinSATResultsInfo.GetAssessmentInfo
title: IProvideWinSATResultsInfo::GetAssessmentInfo (winsatcominterfacei.h)
description: Retrieves summary information for a subcomponent of the assessment.
helpviewer_keywords: ["GetAssessmentInfo","GetAssessmentInfo method [WinSAT]","GetAssessmentInfo method [WinSAT]","IProvideWinSATResultsInfo interface","IProvideWinSATResultsInfo interface [WinSAT]","GetAssessmentInfo method","IProvideWinSATResultsInfo.GetAssessmentInfo","IProvideWinSATResultsInfo::GetAssessmentInfo","winsat.iprovidewinsatresultsinfo_getassessmentinfo","winsatcominterfacei/IProvideWinSATResultsInfo::GetAssessmentInfo"]
old-location: winsat\iprovidewinsatresultsinfo_getassessmentinfo.htm
tech.root: WinSAT
ms.assetid: dfa4d740-2dfd-41b5-a0be-a241f9ece939
ms.date: 12/05/2018
ms.keywords: GetAssessmentInfo, GetAssessmentInfo method [WinSAT], GetAssessmentInfo method [WinSAT],IProvideWinSATResultsInfo interface, IProvideWinSATResultsInfo interface [WinSAT],GetAssessmentInfo method, IProvideWinSATResultsInfo.GetAssessmentInfo, IProvideWinSATResultsInfo::GetAssessmentInfo, winsat.iprovidewinsatresultsinfo_getassessmentinfo, winsatcominterfacei/IProvideWinSATResultsInfo::GetAssessmentInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProvideWinSATResultsInfo::GetAssessmentInfo
 - winsatcominterfacei/IProvideWinSATResultsInfo::GetAssessmentInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IProvideWinSATResultsInfo.GetAssessmentInfo
---

# IProvideWinSATResultsInfo::GetAssessmentInfo


## -description

<p class="CCE_Message">[IProvideWinSATResultsInfo::GetAssessmentInfo may be altered or unavailable for releases after Windows 8.1.]

Retrieves summary information for a subcomponent of the assessment.

## -parameters

### -param assessment [in]

A subcomponent of the assessment whose summary information you want to retrieve. For possible values, see the <a href="/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_type">WINSAT_ASSESSMENT_TYPE</a> enumeration.

### -param ppinfo [out]

An <a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo">IProvideWinSATAssessmentInfo</a> interface that you use to get the score for the subcomponent.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo">IProvideWinSATResultsInfo</a>