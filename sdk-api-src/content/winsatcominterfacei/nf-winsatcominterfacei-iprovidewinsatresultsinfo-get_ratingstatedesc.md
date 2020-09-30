---
UID: NF:winsatcominterfacei.IProvideWinSATResultsInfo.get_RatingStateDesc
title: IProvideWinSATResultsInfo::get_RatingStateDesc (winsatcominterfacei.h)
description: Retrieves a string that you can use in a UI to indicate whether the assessment is valid.
helpviewer_keywords: ["IProvideWinSATResultsInfo interface [WinSAT]","RatingStateDesc property","IProvideWinSATResultsInfo.RatingStateDesc","IProvideWinSATResultsInfo.get_RatingStateDesc","IProvideWinSATResultsInfo::RatingStateDesc","IProvideWinSATResultsInfo::get_RatingStateDesc","RatingStateDesc property [WinSAT]","RatingStateDesc property [WinSAT]","IProvideWinSATResultsInfo interface","get_RatingStateDesc","winsat.iprovidewinsatresultsinfo_ratingstatedesc","winsatcominterfacei/IProvideWinSATResultsInfo::RatingStateDesc","winsatcominterfacei/IProvideWinSATResultsInfo::get_RatingStateDesc"]
old-location: winsat\iprovidewinsatresultsinfo_ratingstatedesc.htm
tech.root: WinSAT
ms.assetid: 6995a4a2-a8c6-4c8f-bac0-478af4d8f911
ms.date: 12/05/2018
ms.keywords: IProvideWinSATResultsInfo interface [WinSAT],RatingStateDesc property, IProvideWinSATResultsInfo.RatingStateDesc, IProvideWinSATResultsInfo.get_RatingStateDesc, IProvideWinSATResultsInfo::RatingStateDesc, IProvideWinSATResultsInfo::get_RatingStateDesc, RatingStateDesc property [WinSAT], RatingStateDesc property [WinSAT],IProvideWinSATResultsInfo interface, get_RatingStateDesc, winsat.iprovidewinsatresultsinfo_ratingstatedesc, winsatcominterfacei/IProvideWinSATResultsInfo::RatingStateDesc, winsatcominterfacei/IProvideWinSATResultsInfo::get_RatingStateDesc
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
 - IProvideWinSATResultsInfo::get_RatingStateDesc
 - winsatcominterfacei/IProvideWinSATResultsInfo::get_RatingStateDesc
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
 - IProvideWinSATResultsInfo.RatingStateDesc
 - IProvideWinSATResultsInfo.get_RatingStateDesc
---

# IProvideWinSATResultsInfo::get_RatingStateDesc


## -description

<p class="CCE_Message">[IProvideWinSATResultsInfo::RatingStateDesc may be altered or unavailable for releases after Windows 8.1.]

Retrieves a string that you can use in a UI to indicate whether the assessment is valid.

This property is read-only.

## -parameters

## -remarks

If the assessment is valid, the string is "Windows Experience Index"; otherwise, the string is "Windows Experience Index : Unrated". To determine the validity of the assessment, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_assessmentstate">IProvideWinSATResultsInfo::get_AssessmentState</a> method.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo">IProvideWinSATResultsInfo</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_assessmentstate">IProvideWinSATResultsInfo::AssessmentState</a>