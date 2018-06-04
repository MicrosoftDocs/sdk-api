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

# ISimilarityReportProgress::ReportProgress


## -description


Reports the current completion percentage of a similarity operation in progress.


## -parameters




### -param percentCompleted [in]

The current completion percentage of the task. The valid range is from 0 through 100.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/3a31530e-da6d-4ac8-9fd4-d91419777ce5">ISimilarity::CopyAndSwap</a> method calls the <b>ReportProgress</b>  method to report the progress of the copy-and-swap operation. To receive the progress information, RDC applications must implement this method.

No guarantee is made as to how frequently this method is called, nor that it will be called with any specific values for the <i>percentCompleted</i> parameter. For example, the <i>percentCompleted</i> parameter may not start at zero and may never reach 100, and it may receive the same value more than once. However, each value is guaranteed to be greater than or equal to the previous value.

If the application returns an error code such as <b>E_FAIL</b>, the similarity operation is stopped, and the error code is propagated.




## -see-also




<a href="https://msdn.microsoft.com/813bda93-08d5-456c-9bde-ce6dd53fb8bf">ISimilarityReportProgress</a>
 

 

