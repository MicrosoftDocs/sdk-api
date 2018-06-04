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

# FilterInstanceFindClose function


## -description


The <b>FilterInstanceFindClose</b> function closes the specified minifilter instance search handle. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a> functions use this search handle to locate instances of a minifilter. 


## -parameters




### -param hFilterInstanceFind [in]

Minifilter instance search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>. 


## -returns



<b>FilterInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterInstanceFindClose</b> function is called, the minifilter instance search handle specified by the <i>hFilterInstanceFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a> or <b>FilterInstanceFindClose</b>. 

Use <b>FilterInstanceFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a>
 

 

