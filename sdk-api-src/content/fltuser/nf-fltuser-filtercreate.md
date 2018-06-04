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

# FilterCreate function


## -description


The <b>FilterCreate</b> function creates a handle for the given minifilter. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter. This parameter is required and cannot be <b>NULL</b>. 


### -param hFilter [out]

Pointer to a caller-allocated variable that receives a handle for the minifilter if the call to <b>FilterCreate</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. 


## -returns



<b>FilterCreate</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



A user-mode application calls <b>FilterCreate</b> to create a handle that can be used to communicate with a kernel-mode minifilter. The returned minifilter handle can be passed as a parameter to functions such as <a href="https://msdn.microsoft.com/library/windows/hardware/ff540500">FilterGetInformation</a>. 

To close a filter handle returned by <b>FilterCreate</b>, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540500">FilterGetInformation</a>
 

 

