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

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info">IQueryRecentWinSATAssessment::get_Info</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideWinSATResultsInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IProvideWinSATResultsInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IProvideWinSATResultsInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">GetAssessmentInfo</a>
</td>
<td align="left" width="63%">
Retrieves summary information for a subcomponent of the assessment.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideWinSATResultsInfo</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_assessmentdatetime">AssessmentDateTime</a>


</td>
<td align="left" width="63%">
Retrieves the date and time that the assessment was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_assessmentstate">AssessmentState</a>


</td>
<td align="left" width="63%">
Retrieves the state of the assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_ratingstatedesc">RatingStateDesc</a>


</td>
<td align="left" width="63%">
Retrieves a string that you can use in a UI that indicates whether the assessment is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating">SystemRating</a>


</td>
<td align="left" width="63%">
Retrieves the base score for the computer.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo">IProvideWinSATAssessmentInfo</a>

