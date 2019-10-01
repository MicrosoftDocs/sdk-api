---
UID: NF:ras.RasInvokeEapUI
title: RasInvokeEapUI function (ras.h)
author: windows-sdk-content
description: The RasInvokeEapUI function displays a custom user interface to obtain Extensible Authentication Protocol (EAP) information from the user.
old-location: rras\rasinvokeeapui.htm
tech.root: RRAS
ms.assetid: 60661c23-3d6a-4b0c-9cc9-bf04ecea2425
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RasInvokeEapUI, RasInvokeEapUI function [RAS], _ras_rasinvokeeapui, ras/RasInvokeEapUI, rras.rasinvokeeapui
ms.topic: function
f1_keywords: 
 - "ras/RasInvokeEapUI"
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasInvokeEapUI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasInvokeEapUI function


## -description


The 
<b>RasInvokeEapUI</b> function displays a custom user interface to obtain Extensible Authentication Protocol (EAP) information from the user.


## -parameters




### -param arg1 [in]

Handle to the connection returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.


### -param arg2 [in]

Specifies the subentry returned in the callback.


### -param arg3 [in]

Pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure. This structure should be the same as that passed to 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> when restarting from a paused state. Ensure that the <b>dwSize</b> member of the 
<b>RASDIALEXTENSIONS</b> structure specifies the size of the structure. Obtain the size using sizeof(<b>RASDIALEXTENSIONS</b>). This parameter cannot be <b>NULL</b>.


### -param arg4 [in]

Handle to the parent window to use when displaying the EAP user interface.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasConn</i> parameter is zero, or the <i>lpExtensions</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The value of the <b>dwSize</b> member of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure specifies a version of the structure that isn't supported by the operating system in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377242(v=vs.85)">RASEAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

