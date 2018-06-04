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

# LoadPerfCounterTextStringsA function


## -description


Loads onto the computer the performance objects and counters defined in the specified initialization file.
		


## -parameters




### -param lpCommandLine

TBD


### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the  <b>Lodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.


#### - commandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the initialization (.ini) file. The name can include the path to the initialization file. 

The function uses only the initialization file; the first argument is discarded. For example, to load an initialization file called "myfile.ini", the <i>commandLine</i> string could be "xx myfile.ini". The letters before the space (here "xx")  are discarded, and the second part, following the space, is interpreted as the initialization file specification.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by the <b>Lodctr</b> tool. For information on <b>Lodctr</b>, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/f78858ca-d8d0-4178-9f9a-731b89cf5a61">UnloadPerfCounterTextStrings</a>
 

 

