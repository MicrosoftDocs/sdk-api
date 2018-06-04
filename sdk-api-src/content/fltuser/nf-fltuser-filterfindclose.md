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

# FilterFindClose function


## -description


The <b>FilterFindClose</b> function closes the specified minifilter search handle. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a> functions use this search handle to locate minifilters. 


## -parameters




### -param hFilterFind [in]

Minifilter search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>. 


## -returns



<b>FilterFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterFindClose</b> function is called, the minifilter search handle specified by the <i>hFilterFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a> or <b>FilterFindClose</b>. 

Use <b>FilterFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a>
 

 

