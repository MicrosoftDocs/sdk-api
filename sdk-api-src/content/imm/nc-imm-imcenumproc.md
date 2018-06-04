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

# IMCENUMPROC callback function


## -description


An application-defined callback function that processes input contexts provided by the <a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a> function. The IMCENUMPROC type defines a pointer to this callback function. <b>EnumInputContext</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - hIMC [in]

Handle to the input context.


#### - lParam [in]

Application-supplied data.


## -returns



Returns a nonzero value to continue enumeration, or 0 to stop enumeration.




## -remarks



An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

