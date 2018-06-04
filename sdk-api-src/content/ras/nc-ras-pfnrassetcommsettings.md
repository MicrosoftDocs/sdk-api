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

# PFNRASSETCOMMSETTINGS callback function


## -description


Call 
<b>RasSetCommSettings</b> from a custom-scripting DLL to change the settings on the port for the connection.


## -parameters




### -param hPort [in]

Handle to the port on which to apply the settings. This handle is passed to the custom-scripting DLL in the 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a> function.


### -param *pRasCommSettings [in]

Pointer to a 
<a href="https://msdn.microsoft.com/20fd0533-2ce4-4832-abfd-0b37d3887249">RASCOMMSETTINGS</a> structure that specifies the settings to be applied to the port.


### -param pvReserved [in]

Reserved for future use. This parameter must be <b>NULL</b>.


## -returns



This callback function does not return a value.




## -remarks



RAS passes the custom-scripting DLL a pointer to the 
<b>RasSetCommSettings</b> function when RAS calls 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>. The pointer is stored in the 
<a href="https://msdn.microsoft.com/e143c1d7-1d4a-43e6-b099-3b65bb30dc06">RASCUSTOMSCRIPTEXTENSIONS</a> structure that is passed as the last parameter of 
<b>RasCustomScriptExecute</b>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/20fd0533-2ce4-4832-abfd-0b37d3887249">RASCOMMSETTINGS</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>
 

 

