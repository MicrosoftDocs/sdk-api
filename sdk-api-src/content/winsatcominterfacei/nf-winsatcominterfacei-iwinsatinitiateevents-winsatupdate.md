---
UID: NF:winsatcominterfacei.IWinSATInitiateEvents.WinSATUpdate
title: IWinSATInitiateEvents::WinSATUpdate
author: windows-sdk-content
description: Receives notification when an assessment is making progress.
old-location: winsat\iwinsatinitiateevents_winsatupdate.htm
old-project: WinSAT
ms.assetid: d0f527a9-89b9-45d6-b5a5-82b0ae1ad122
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWinSATInitiateEvents interface [WinSAT],WinSATUpdate method, IWinSATInitiateEvents.WinSATUpdate, IWinSATInitiateEvents::WinSATUpdate, WinSATUpdate, WinSATUpdate method [WinSAT], WinSATUpdate method [WinSAT],IWinSATInitiateEvents interface, winsat.iwinsatinitiateevents_winsatupdate, winsatcominterfacei/IWinSATInitiateEvents::WinSATUpdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsatcominterfacei.h
req.include-header: 
req.redist: 
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
 - IWinSATInitiateEvents.WinSATUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWinSATInitiateEvents::WinSATUpdate


## -description


<p class="CCE_Message">[IWinSATInitiateEvents::WinSATUpdate may be altered or unavailable for releases after Windows 8.1.]

Receives notification when an assessment is making progress.


## -parameters




### -param uCurrentTick [in]

The current progress tick of the assessment.


### -param uTickTotal [in]

The total number of progress ticks for the assessment.


### -param strCurrentState [in]

A string that contains the current state of the assessment. This string is valid during the life of this callback. Copy the string if you need it after the callback returns.


## -returns



This method should return  S_OK; the value is ignored.




## -remarks



You can use this method to determine the progress of a formal assessment.  

<div class="alert"><b>Note</b>  You can use the <i>uCurrentTick</i> and <i>uTickTotal</i> values to mark progress for formal assessments only; the values are zero for all other assessments.</div>
<div> </div>
You should keep your implementation short so you do not miss subsequent updates; you will not get new updates until the method returns.

<div class="alert"><b>Note</b>  If an instance of WinSAT is already running, it is possible that you could receive one or more update callbacks for the currently running assessment.</div>
<div> </div>

#### Examples

For an example implementation, see the <a href="https://msdn.microsoft.com/c57d88b6-81ac-4314-8593-59a950348be4">InitiateAssessment</a> or <a href="https://msdn.microsoft.com/9425e41c-fe03-4c94-a5eb-686775b5fce7">InitiateFormalAssessment</a> method of <a href="https://msdn.microsoft.com/0b299477-50a4-4f61-a0e5-fdbae239503b">IInitiateWinSATAssessment</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0b299477-50a4-4f61-a0e5-fdbae239503b">IInitiateWinSATAssessment</a>



<a href="https://msdn.microsoft.com/f6ab3284-a76f-4148-ae40-04aa782ea9a7">IWinSATInitiateEvents</a>



<a href="https://msdn.microsoft.com/a7bcd7e6-b8d7-4ec3-84e8-8ccbcd0b4ada">IWinSATInitiateEvents::WinSATComplete</a>
 

 

