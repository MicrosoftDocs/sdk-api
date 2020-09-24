---
UID: NN:winsatcominterfacei.IQueryRecentWinSATAssessment
title: IQueryRecentWinSATAssessment (winsatcominterfacei.h)
description: Retrieves details about the results of the most recent formal WinSAT assessment.
helpviewer_keywords: ["IQueryRecentWinSATAssessment","IQueryRecentWinSATAssessment interface [WinSAT]","IQueryRecentWinSATAssessment interface [WinSAT]","described","winsat.iqueryrecentwinsatassessment","winsatcominterfacei/IQueryRecentWinSATAssessment"]
old-location: winsat\iqueryrecentwinsatassessment.htm
tech.root: WinSAT
ms.assetid: 6849d8b6-d192-4520-a737-39e22e14a70f
ms.date: 12/05/2018
ms.keywords: IQueryRecentWinSATAssessment, IQueryRecentWinSATAssessment interface [WinSAT], IQueryRecentWinSATAssessment interface [WinSAT],described, winsat.iqueryrecentwinsatassessment, winsatcominterfacei/IQueryRecentWinSATAssessment
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
 - IQueryRecentWinSATAssessment
 - winsatcominterfacei/IQueryRecentWinSATAssessment
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
 - IQueryRecentWinSATAssessment
---

# IQueryRecentWinSATAssessment interface


## -description

<p class="CCE_Message">[IQueryRecentWinSATAssessment may be altered or unavailable for releases after Windows 8.1.]

Retrieves details about the results of the most recent formal WinSAT assessment.

To retrieve this interface, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CQueryWinSAT) as the class identifier and __uuidof(IQueryRecentWinSATAssessment) as the interface identifier.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryallwinsatassessments">IQueryAllWinSATAssessments</a>