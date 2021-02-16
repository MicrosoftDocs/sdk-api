---
UID: NF:winsatcominterfacei.IProvideWinSATAssessmentInfo.get_Title
title: IProvideWinSATAssessmentInfo::get_Title (winsatcominterfacei.h)
description: Retrieves the title of the subcomponent.
helpviewer_keywords: ["IProvideWinSATAssessmentInfo interface [WinSAT]","Title property","IProvideWinSATAssessmentInfo.Title","IProvideWinSATAssessmentInfo.get_Title","IProvideWinSATAssessmentInfo::Title","IProvideWinSATAssessmentInfo::get_Title","Title property [WinSAT]","Title property [WinSAT]","IProvideWinSATAssessmentInfo interface","get_Title","winsat.iprovidewinsatassessmentinfo_title","winsatcominterfacei/IProvideWinSATAssessmentInfo::Title","winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Title"]
old-location: winsat\iprovidewinsatassessmentinfo_title.htm
tech.root: WinSAT
ms.assetid: 11c9c59f-97d6-41d1-ab0e-7901e126b07c
ms.date: 12/05/2018
ms.keywords: IProvideWinSATAssessmentInfo interface [WinSAT],Title property, IProvideWinSATAssessmentInfo.Title, IProvideWinSATAssessmentInfo.get_Title, IProvideWinSATAssessmentInfo::Title, IProvideWinSATAssessmentInfo::get_Title, Title property [WinSAT], Title property [WinSAT],IProvideWinSATAssessmentInfo interface, get_Title, winsat.iprovidewinsatassessmentinfo_title, winsatcominterfacei/IProvideWinSATAssessmentInfo::Title, winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Title
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
 - IProvideWinSATAssessmentInfo::get_Title
 - winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Title
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
 - IProvideWinSATAssessmentInfo.Title
 - IProvideWinSATAssessmentInfo.get_Title
---

# IProvideWinSATAssessmentInfo::get_Title


## -description

<p class="CCE_Message">[IProvideWinSATAssessmentInfo::Title may be altered or unavailable for releases after Windows 8.1.]

Retrieves the title of the subcomponent.

This property is read-only.

## -parameters

## -remarks

Note that the title includes a trailing colon character. For example, the title for the CPU subcomponent is "Processor:".


#### Examples

For an example, see the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo">IProvideWinSATAssessmentInfo</a>