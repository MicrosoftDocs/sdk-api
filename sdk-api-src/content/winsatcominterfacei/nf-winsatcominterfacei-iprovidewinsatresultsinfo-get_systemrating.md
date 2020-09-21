---
UID: NF:winsatcominterfacei.IProvideWinSATResultsInfo.get_SystemRating
title: IProvideWinSATResultsInfo::get_SystemRating (winsatcominterfacei.h)
description: Retrieves the base score for the computer.
helpviewer_keywords: ["IProvideWinSATResultsInfo interface [WinSAT]","SystemRating property","IProvideWinSATResultsInfo.SystemRating","IProvideWinSATResultsInfo.get_SystemRating","IProvideWinSATResultsInfo::SystemRating","IProvideWinSATResultsInfo::get_SystemRating","SystemRating property [WinSAT]","SystemRating property [WinSAT]","IProvideWinSATResultsInfo interface","get_SystemRating","winsat.iprovidewinsatresultsinfo_systemrating","winsatcominterfacei/IProvideWinSATResultsInfo::SystemRating","winsatcominterfacei/IProvideWinSATResultsInfo::get_SystemRating"]
old-location: winsat\iprovidewinsatresultsinfo_systemrating.htm
tech.root: WinSAT
ms.assetid: 4fe20830-bf86-4551-ba73-534740cabab5
ms.date: 12/05/2018
ms.keywords: IProvideWinSATResultsInfo interface [WinSAT],SystemRating property, IProvideWinSATResultsInfo.SystemRating, IProvideWinSATResultsInfo.get_SystemRating, IProvideWinSATResultsInfo::SystemRating, IProvideWinSATResultsInfo::get_SystemRating, SystemRating property [WinSAT], SystemRating property [WinSAT],IProvideWinSATResultsInfo interface, get_SystemRating, winsat.iprovidewinsatresultsinfo_systemrating, winsatcominterfacei/IProvideWinSATResultsInfo::SystemRating, winsatcominterfacei/IProvideWinSATResultsInfo::get_SystemRating
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
 - IProvideWinSATResultsInfo::get_SystemRating
 - winsatcominterfacei/IProvideWinSATResultsInfo::get_SystemRating
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
 - IProvideWinSATResultsInfo.SystemRating
 - IProvideWinSATResultsInfo.get_SystemRating
---

# IProvideWinSATResultsInfo::get_SystemRating


## -description

<p class="CCE_Message">[IProvideWinSATResultsInfo::SystemRating may be altered or unavailable for releases after Windows 8.1.]

Retrieves the base score for the computer.

This property is read-only.

## -parameters

## -remarks

The Windows Experience Index feature measures the capability of your computer's hardware configuration and expresses this measurement as a number called a base score. A higher base score generally means that your computer will perform better and faster than a computer with a lower base score, especially when performing more advanced and resource-intensive tasks. 



Each hardware component receives an individual subscore. Your computer's base score is determined by the lowest subscore. For example, if the lowest subscore of an individual hardware component is 2.6, then the base score is 2.6. The base score is not an average of the combined subscores.



You can use the base score to confidently buy programs and other software that are matched to your computer's base score. For example, if your computer has a base score of 3.3, then you can confidently purchase any software designed for this version of Windows that requires a computer with a base score of 3 or lower.


To get the score for a subcomponent of the assessment, such as the CPU, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score">IProvideWinSATAssessmentInfo::get_Score</a> method.


#### Examples

For an example, see the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info">IQueryRecentWinSATAssessment::Info</a> property.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo">IProvideWinSATResultsInfo</a>



<a href="/windows/desktop/WinSAT/win32-winsat">Win32_WinSAT</a>