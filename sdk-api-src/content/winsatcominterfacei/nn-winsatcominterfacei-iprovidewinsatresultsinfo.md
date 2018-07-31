---
UID: NN:winsatcominterfacei.IProvideWinSATResultsInfo
title: IProvideWinSATResultsInfo
author: windows-sdk-content
description: Gets information about the results of an assessment, for example, the base score and the date that the assessment was run.
old-location: winsat\iprovidewinsatresultsinfo.htm
old-project: WinSAT
ms.assetid: bd15bc63-a918-43a7-9864-4206a0b6af84
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IProvideWinSATResultsInfo, IProvideWinSATResultsInfo interface [WinSAT], IProvideWinSATResultsInfo interface [WinSAT],described, winsat.iprovidewinsatresultsinfo, winsatcominterfacei/IProvideWinSATResultsInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IProvideWinSATResultsInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IProvideWinSATResultsInfo interface


## -description


<p class="CCE_Message">[IProvideWinSATResultsInfo may be altered or unavailable for releases after Windows 8.1.]

Gets information about the results of an assessment, for example, the base score and the date that the assessment was run.

To get this interface, call the <a href="https://msdn.microsoft.com/11697416-aa4d-4724-bd63-8d123e2b32cb">IQueryRecentWinSATAssessment::get_Info</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideWinSATResultsInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IProvideWinSATResultsInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">GetAssessmentInfo</a>
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

<a href="https://msdn.microsoft.com/c5fcf832-7290-45dc-9c36-7b469dc54a4c">AssessmentDateTime</a>


</td>
<td align="left" width="63%">
Retrieves the date and time that the assessment was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">AssessmentState</a>


</td>
<td align="left" width="63%">
Retrieves the state of the assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6995a4a2-a8c6-4c8f-bac0-478af4d8f911">RatingStateDesc</a>


</td>
<td align="left" width="63%">
Retrieves a string that you can use in a UI that indicates whether the assessment is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4fe20830-bf86-4551-ba73-534740cabab5">SystemRating</a>


</td>
<td align="left" width="63%">
Retrieves the base score for the computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90036c75-6e9e-4d25-804b-02c423616de1">IProvideWinSATAssessmentInfo</a>
 

 

