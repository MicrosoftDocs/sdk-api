---
UID: NC:ras.PFNRASSETCOMMSETTINGS
title: PFNRASSETCOMMSETTINGS
author: windows-sdk-content
description: Call RasSetCommSettings from a custom-scripting DLL to change the settings on the port for the connection.
old-location: rras\rassetcommsettings.htm
old-project: RRAS
ms.assetid: 1df305b8-39b0-4426-b20a-62aa79240f67
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PFNRASSETCOMMSETTINGS, PFNRASSETCOMMSETTINGS callback, RasSetCommSettings, RasSetCommSettings callback function [RAS], _ras_rassetcommsettings, ras/RasSetCommSettings, rras.rassetcommsettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ras.h
api_name:
-	RasSetCommSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

