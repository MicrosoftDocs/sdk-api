---
UID: NF:ras.RasInvokeEapUI
title: RasInvokeEapUI function
author: windows-sdk-content
description: The RasInvokeEapUI function displays a custom user interface to obtain Extensible Authentication Protocol (EAP) information from the user.
old-location: rras\rasinvokeeapui.htm
old-project: rras
ms.assetid: 60661c23-3d6a-4b0c-9cc9-bf04ecea2425
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasInvokeEapUI, RasInvokeEapUI function [RAS], _ras_rasinvokeeapui, ras/RasInvokeEapUI, rras.rasinvokeeapui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasInvokeEapUI
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasInvokeEapUI function


## -description


The 
<b>RasInvokeEapUI</b> function displays a custom user interface to obtain Extensible Authentication Protocol (EAP) information from the user.


## -parameters




### -param

TBD




#### - [in]

Handle to the connection returned by 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>.


#### - dwSubEntry [in]

Specifies the subentry returned in the callback.


#### - lpExtensions [in]

Pointer to the 
<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a> structure. This structure should be the same as that passed to 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> when restarting from a paused state. Ensure that the <b>dwSize</b> member of the 
<b>RASDIALEXTENSIONS</b> structure specifies the size of the structure. Obtain the size using sizeof(<b>RASDIALEXTENSIONS</b>). This parameter cannot be <b>NULL</b>.


#### - hwnd [in]

Handle to the parent window to use when displaying the EAP user interface.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a> structure specifies a version of the structure that isn't supported by the operating system in use.

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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a>



<a href="https://msdn.microsoft.com/b5f28e70-845e-49be-9bb2-99691dc0fcf1">RASEAPINFO</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

