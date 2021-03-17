---
UID: NN:winsatcominterfacei.IProvideWinSATAssessmentInfo
title: IProvideWinSATAssessmentInfo (winsatcominterfacei.h)
description: Gets summary information for a subcomponent of the assessment, for example, its score.
helpviewer_keywords: ["IProvideWinSATAssessmentInfo","IProvideWinSATAssessmentInfo interface [WinSAT]","IProvideWinSATAssessmentInfo interface [WinSAT]","described","winsat.iprovidewinsatassessmentinfo","winsatcominterfacei/IProvideWinSATAssessmentInfo"]
old-location: winsat\iprovidewinsatassessmentinfo.htm
tech.root: WinSAT
ms.assetid: 90036c75-6e9e-4d25-804b-02c423616de1
ms.date: 12/05/2018
ms.keywords: IProvideWinSATAssessmentInfo, IProvideWinSATAssessmentInfo interface [WinSAT], IProvideWinSATAssessmentInfo interface [WinSAT],described, winsat.iprovidewinsatassessmentinfo, winsatcominterfacei/IProvideWinSATAssessmentInfo
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
 - IProvideWinSATAssessmentInfo
 - winsatcominterfacei/IProvideWinSATAssessmentInfo
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
 - IProvideWinSATAssessmentInfo
---

# IProvideWinSATAssessmentInfo interface


## -description

<p class="CCE_Message">[IProvideWinSATAssessmentInfo may be altered or unavailable for releases after Windows 8.1.]

Gets summary information for a subcomponent of the assessment, for example, its score.

To get this interface, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.

## -remarks

To retrieve details of the subcomponent, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml">IQueryRecentWinSATAssessment::get_XML</a> method.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo">IProvideWinSATResultsInfo</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a>