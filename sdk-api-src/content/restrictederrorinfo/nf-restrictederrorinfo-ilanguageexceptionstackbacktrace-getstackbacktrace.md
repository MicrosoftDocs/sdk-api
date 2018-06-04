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

# ILanguageExceptionStackBackTrace::GetStackBackTrace


## -description


Retrieves the back stack trace.


## -parameters




### -param maxFramesToCapture [in]

The maximum number of frames to capture.


### -param stackBackTrace [in, out]

An array containing the stack back trace; the maximum size is the <i>maxFramesToCapture</i>.


### -param framesCaptured [out]

On success, contains a pointer to the number of frames actually captured.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You should implement <b>GetStackBackTrace</b> in your language projections when the Global Error Handler surface is unable to capture a backtrace. <b>GetStackBackTrace</b> is called by the <a href="https://msdn.microsoft.com/573A9209-31EF-4FD4-A504-16795BA42337">RoOriginateLanguageException</a> export and by <a href="https://msdn.microsoft.com/60026962-4E6C-4906-97D9-46BD2BCA3AC6">CapturePropagationContext</a> when those functions detect, through querying for interface (QI), that the language exception provided to them implements it. 





## -see-also




<a href="https://msdn.microsoft.com/A5AA17A2-414B-4641-A417-4F73384216F9">ILanguageExceptionStackBackTrace</a>
 

 

