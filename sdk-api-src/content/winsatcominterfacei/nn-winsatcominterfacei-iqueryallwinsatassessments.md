---
UID: NN:winsatcominterfacei.IQueryAllWinSATAssessments
title: IQueryAllWinSATAssessments (winsatcominterfacei.h)
description: Retrieves details about all formal WinSAT assessments.
helpviewer_keywords: ["IQueryAllWinSATAssessments","IQueryAllWinSATAssessments interface [WinSAT]","IQueryAllWinSATAssessments interface [WinSAT]","described","winsat.iqueryallwinsatassessments","winsatcominterfacei/IQueryAllWinSATAssessments"]
old-location: winsat\iqueryallwinsatassessments.htm
tech.root: WinSAT
ms.assetid: b78cfaf1-0fce-449c-96f5-76d318f30384
ms.date: 12/05/2018
ms.keywords: IQueryAllWinSATAssessments, IQueryAllWinSATAssessments interface [WinSAT], IQueryAllWinSATAssessments interface [WinSAT],described, winsat.iqueryallwinsatassessments, winsatcominterfacei/IQueryAllWinSATAssessments
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
 - IQueryAllWinSATAssessments
 - winsatcominterfacei/IQueryAllWinSATAssessments
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
 - IQueryAllWinSATAssessments
---

# IQueryAllWinSATAssessments interface


## -description

<p class="CCE_Message">[IQueryAllWinSATAssessments may be altered or unavailable for releases after Windows 8.1.]

Retrieves details about all formal WinSAT assessments.

To retrieve this interface, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CQueryAllWinSAT) as the class identifier and __uuidof(IQueryAllWinSATAssessments) as the interface identifier.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a>