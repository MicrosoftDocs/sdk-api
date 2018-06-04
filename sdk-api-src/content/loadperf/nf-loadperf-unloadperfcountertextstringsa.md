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

# UnloadPerfCounterTextStringsA function


## -description


Unloads performance objects and counters from the computer for the specified application.
		


## -parameters




### -param lpCommandLine

TBD


### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the  <b>Unlodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.


#### - commandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the application. The name of the application must match the <b>drivername</b> key value found in the initialization (.ini) file used to <a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">load the text strings</a>.


## -returns




						If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by <b>Unlodctr</b> tool. For more information, see <a href="https://msdn.microsoft.com/83c0fb91-857c-40d9-8fb8-8734c1b573c4">Removing Counter Names and Descriptions from the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">LoadPerfCounterTextStrings</a>
 

 

