---
UID: NF:winsatcominterfacei.IProvideWinSATAssessmentInfo.get_Title
title: IProvideWinSATAssessmentInfo::get_Title
author: windows-sdk-content
description: Retrieves the title of the subcomponent.
old-location: winsat\iprovidewinsatassessmentinfo_title.htm
tech.root: WinSAT
ms.assetid: 11c9c59f-97d6-41d1-ab0e-7901e126b07c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IProvideWinSATAssessmentInfo interface [WinSAT],Title property, IProvideWinSATAssessmentInfo.Title, IProvideWinSATAssessmentInfo.get_Title, IProvideWinSATAssessmentInfo::Title, IProvideWinSATAssessmentInfo::get_Title, Title property [WinSAT], Title property [WinSAT],IProvideWinSATAssessmentInfo interface, get_Title, winsat.iprovidewinsatassessmentinfo_title, winsatcominterfacei/IProvideWinSATAssessmentInfo::Title, winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Title
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IProvideWinSATAssessmentInfo.Title
 - IProvideWinSATAssessmentInfo.get_Title
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

For an example, see the <a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/90036c75-6e9e-4d25-804b-02c423616de1">IProvideWinSATAssessmentInfo</a>
 

 

