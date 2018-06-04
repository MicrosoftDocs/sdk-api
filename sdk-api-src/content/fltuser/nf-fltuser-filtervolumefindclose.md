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

# FilterVolumeFindClose function


## -description


The <b>FilterVolumeFindClose</b> function closes the specified volume search handle. <a href="https://msdn.microsoft.com/library/windows/hardware/ff541525">FilterVolumeFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff541530">FilterVolumeFindNext</a> use this search handle to locate volumes. 


## -parameters




### -param hVolumeFind [in]

Volume search handle to close. This handle must have been previously opened by <a href="https://msdn.microsoft.com/library/windows/hardware/ff541525">FilterVolumeFindFirst</a>. 


## -returns



<b>FilterVolumeFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterVolumeFindClose</b> function is called, the handle specified by the <i>hVolumeFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff541530">FilterVolumeFindNext</a> or <b>FilterVolumeFindClose</b>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541525">FilterVolumeFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541530">FilterVolumeFindNext</a>
 

 

