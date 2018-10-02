---
UID: NN:winsatcominterfacei.IWinSATInitiateEvents
title: IWinSATInitiateEvents
author: windows-sdk-content
description: Implement this interface to receive notifications when an assessment is complete or making progress.
old-location: winsat\iwinsatinitiateevents.htm
tech.root: WinSAT
ms.assetid: f6ab3284-a76f-4148-ae40-04aa782ea9a7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWinSATInitiateEvents, IWinSATInitiateEvents interface [WinSAT], IWinSATInitiateEvents interface [WinSAT],described, winsat.iwinsatinitiateevents, winsatcominterfacei/IWinSATInitiateEvents
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
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IWinSATInitiateEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWinSATInitiateEvents interface


## -description


<p class="CCE_Message">[IWinSATInitiateEvents may be altered or unavailable for releases after Windows 8.1.]

Implement this interface to receive notifications when an assessment is complete or making progress.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinSATInitiateEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWinSATInitiateEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWinSATInitiateEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7bcd7e6-b8d7-4ec3-84e8-8ccbcd0b4ada">WinSATComplete</a>
</td>
<td align="left" width="63%">
Receives notification  when an assessment succeeds, fails, or is canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0f527a9-89b9-45d6-b5a5-82b0ae1ad122">WinSATUpdate</a>
</td>
<td align="left" width="63%">
Receives notification  when an assessment is making progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c57d88b6-81ac-4314-8593-59a950348be4">IInitiateWinSATAssessment::InitiateAssessment</a>



<a href="https://msdn.microsoft.com/9425e41c-fe03-4c94-a5eb-686775b5fce7">IInitiateWinSATAssessment::InitiateFormalAssessment</a>
 

 

