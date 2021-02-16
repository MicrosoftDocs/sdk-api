---
UID: NC:ras.PFNRASSETCOMMSETTINGS
title: PFNRASSETCOMMSETTINGS (ras.h)
description: Call RasSetCommSettings from a custom-scripting DLL to change the settings on the port for the connection.
helpviewer_keywords: ["PFNRASSETCOMMSETTINGS","PFNRASSETCOMMSETTINGS callback","RasSetCommSettings","RasSetCommSettings callback function [RAS]","_ras_rassetcommsettings","ras/RasSetCommSettings","rras.rassetcommsettings"]
old-location: rras\rassetcommsettings.htm
tech.root: RRAS
ms.assetid: 1df305b8-39b0-4426-b20a-62aa79240f67
ms.date: 12/05/2018
ms.keywords: PFNRASSETCOMMSETTINGS, PFNRASSETCOMMSETTINGS callback, RasSetCommSettings, RasSetCommSettings callback function [RAS], _ras_rassetcommsettings, ras/RasSetCommSettings, rras.rassetcommsettings
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNRASSETCOMMSETTINGS
 - ras/PFNRASSETCOMMSETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasSetCommSettings
---

# PFNRASSETCOMMSETTINGS callback function


## -description

Call 
<b>RasSetCommSettings</b> from a custom-scripting DLL to change the settings on the port for the connection.

## -parameters

### -param hPort [in]

Handle to the port on which to apply the settings. This handle is passed to the custom-scripting DLL in the 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a> function.

### -param pRasCommSettings [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa376724(v=vs.85)">RASCOMMSETTINGS</a> structure that specifies the settings to be applied to the port.

### -param pvReserved [in]

Reserved for future use. This parameter must be <b>NULL</b>.

## -returns

This callback function does not return a value.

## -remarks

RAS passes the custom-scripting DLL a pointer to the 
<b>RasSetCommSettings</b> function when RAS calls 
<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>. The pointer is stored in the 
<a href="/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)">RASCUSTOMSCRIPTEXTENSIONS</a> structure that is passed as the last parameter of 
<b>RasCustomScriptExecute</b>.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/previous-versions/windows/desktop/legacy/aa376724(v=vs.85)">RASCOMMSETTINGS</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomscriptexecutefn">RasCustomScriptExecute</a>
