---
UID: NF:winsatcominterfacei.IProvideWinSATResultsInfo.get_RatingStateDesc
title: IProvideWinSATResultsInfo::get_RatingStateDesc
author: windows-driver-content
description: Retrieves a string that you can use in a UI to indicate whether the assessment is valid.
old-location: winsat\iprovidewinsatresultsinfo_ratingstatedesc.htm
old-project: WinSAT
ms.assetid: 6995a4a2-a8c6-4c8f-bac0-478af4d8f911
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IProvideWinSATResultsInfo interface [WinSAT],RatingStateDesc property, IProvideWinSATResultsInfo.RatingStateDesc, IProvideWinSATResultsInfo.get_RatingStateDesc, IProvideWinSATResultsInfo::RatingStateDesc, IProvideWinSATResultsInfo::get_RatingStateDesc, RatingStateDesc property [WinSAT], RatingStateDesc property [WinSAT],IProvideWinSATResultsInfo interface, get_RatingStateDesc, winsat.iprovidewinsatresultsinfo_ratingstatedesc, winsatcominterfacei/IProvideWinSATResultsInfo::RatingStateDesc, winsatcominterfacei/IProvideWinSATResultsInfo::get_RatingStateDesc
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
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Winsatapi.dll
api_name:
-	IProvideWinSATResultsInfo.RatingStateDesc
-	IProvideWinSATResultsInfo.get_RatingStateDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IProvideWinSATResultsInfo::get_RatingStateDesc


## -description


<p class="CCE_Message">[IProvideWinSATResultsInfo::RatingStateDesc may be altered or unavailable for releases after Windows 8.1.]

Retrieves a string that you can use in a UI to indicate whether the assessment is valid.

This property is read-only.


## -parameters


## -remarks



If the assessment is valid, the string is "Windows Experience Index"; otherwise, the string is "Windows Experience Index : Unrated". To determine the validity of the assessment, call the <a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::get_AssessmentState</a> method.




## -see-also




<a href="https://msdn.microsoft.com/bd15bc63-a918-43a7-9864-4206a0b6af84">IProvideWinSATResultsInfo</a>



<a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::AssessmentState</a>
 

 

