---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MFCancelWorkItem function


## -description



          Attempts to cancel an asynchronous operation that was scheduled with <a href="https://msdn.microsoft.com/c14786e4-7fbe-4748-a6ba-e9e68f78b241">MFScheduleWorkItem</a> or <a href="https://msdn.microsoft.com/b698cae1-4f3b-4649-b6f7-583f223eb90c">MFScheduleWorkItemEx</a>.


## -parameters




### -param Key [in]


            The key that was received in the <i>pKey</i> parameter of the <a href="https://msdn.microsoft.com/c14786e4-7fbe-4748-a6ba-e9e68f78b241">MFScheduleWorkItem</a>, <a href="https://msdn.microsoft.com/b698cae1-4f3b-4649-b6f7-583f223eb90c">MFScheduleWorkItemEx</a>, or <a href="https://msdn.microsoft.com/BBD80C60-E42F-4B3B-96E3-E01058A27DB8">MFPutWaitingWorkItem</a> functions.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because work items are asynchronous, the  work-item callback might still be invoked after <b>MFCancelWorkItem</b> is called.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

