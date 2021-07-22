---
UID: NN:winsatcominterfacei.IProvideWinSATResultsInfo
title: IProvideWinSATResultsInfo (winsatcominterfacei.h)
description: Gets information about the results of an assessment, for example, the base score and the date that the assessment was run.
helpviewer_keywords: ["IProvideWinSATResultsInfo","IProvideWinSATResultsInfo interface [WinSAT]","IProvideWinSATResultsInfo interface [WinSAT]","described","winsat.iprovidewinsatresultsinfo","winsatcominterfacei/IProvideWinSATResultsInfo"]
old-location: winsat\iprovidewinsatresultsinfo.htm
tech.root: WinSAT
ms.assetid: bd15bc63-a918-43a7-9864-4206a0b6af84
ms.date: 12/05/2018
ms.keywords: IProvideWinSATResultsInfo, IProvideWinSATResultsInfo interface [WinSAT], IProvideWinSATResultsInfo interface [WinSAT],described, winsat.iprovidewinsatresultsinfo, winsatcominterfacei/IProvideWinSATResultsInfo
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
 - IProvideWinSATResultsInfo
 - winsatcominterfacei/IProvideWinSATResultsInfo
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
 - IProvideWinSATResultsInfo
---

# IProvideWinSATResultsInfo interface


## -description

<p class="CCE_Message">[IProvideWinSATResultsInfo may be altered or unavailable for releases after Windows 8.1.]

Gets information about the results of an assessment, for example, the base score and the date that the assessment was run.

To get this interface, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info">IQueryRecentWinSATAssessment::get_Info</a> method.

## -inheritance

The <b>IProvideWinSATResultsInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IProvideWinSATResultsInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo">IProvideWinSATAssessmentInfo</a>
