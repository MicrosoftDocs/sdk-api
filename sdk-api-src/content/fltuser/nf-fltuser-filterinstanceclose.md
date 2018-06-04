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

# FilterInstanceClose function


## -description


The <b>FilterInstanceClose</b> function closes a minifilter instance handle opened by <b>FilterInstanceCreate</b>. 


## -parameters




### -param hInstance

TBD




#### - hFilterInstanceFind [in]

Minifilter instance handle returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>. 


## -returns



<b>FilterInstanceClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterInstanceClose</b> function is called, the minifilter instance handle specified by the <i>hFilterInstanceFind</i> parameter is no longer valid and cannot safely be used. 

Use <b>FilterInstanceClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540538">FilterInstanceFindClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540538">FilterInstanceFindClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>
 

 

