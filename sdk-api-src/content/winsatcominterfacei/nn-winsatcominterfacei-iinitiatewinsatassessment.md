---
UID: NN:winsatcominterfacei.IInitiateWinSATAssessment
title: IInitiateWinSATAssessment
author: windows-driver-content
description: Initiates an assessment.
old-location: winsat\iinitiatewinsatassessment.htm
old-project: WinSAT
ms.assetid: 0b299477-50a4-4f61-a0e5-fdbae239503b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IInitiateWinSATAssessment, IInitiateWinSATAssessment interface [WinSAT], IInitiateWinSATAssessment interface [WinSAT],described, winsat.iinitiatewinsatassessment, winsatcominterfacei/IInitiateWinSATAssessment
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Winsatapi.dll
api_name:
-	IInitiateWinSATAssessment
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IInitiateWinSATAssessment interface


## -description


<p class="CCE_Message">[IInitiateWinSATAssessment may be altered or unavailable for releases after Windows 8.1.]

Initiates an assessment.

To retrieve this interface, call the <a href="_com_cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CInitiateWinSAT) as the class identifier and __uuidof(IInitiateWinSATAssessment) as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitiateWinSATAssessment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitiateWinSATAssessment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitiateWinSATAssessment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4b159f-9d40-445f-bd43-5fc2e7b2d33b">CancelAssessment</a>
</td>
<td align="left" width="63%">
Cancels a currently running assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c57d88b6-81ac-4314-8593-59a950348be4">InitiateAssessment</a>
</td>
<td align="left" width="63%">
Initiates an ad hoc assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9425e41c-fe03-4c94-a5eb-686775b5fce7">InitiateFormalAssessment</a>
</td>
<td align="left" width="63%">
Initiates a formal assessment.

</td>
</tr>
</table> 

