---
UID: NF:mprapi.MprAdminPortClearStats
title: MprAdminPortClearStats function
author: windows-sdk-content
description: The MprAdminPortClearStats function resets the statistics for the specified port.
old-location: rras\mpradminportclearstats.htm
tech.root: RRAS
ms.assetid: dd932134-7954-4e0a-8170-1dea4ce82011
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MprAdminPortClearStats, MprAdminPortClearStats function [RAS], _mpr_mpradminportclearstats, mprapi/MprAdminPortClearStats, rras.mpradminportclearstats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminPortClearStats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminPortClearStats function


## -description


The 
<b>MprAdminPortClearStats</b> function resets the statistics for the specified port.


## -parameters




### -param hRasServer [in]

Handle to the RAS server on which to clear the statistics for the specified port. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hPort [in]

Handle to the port for which statistics are reset. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/b6caa1f0-f4c7-48a9-b1e8-b484e7d7a3a3">MprAdminPortEnum</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running, possibly because the Dynamic Interface Manager (DIM) is configured to run only on a LAN.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The handle to the RAS server or the handle to the port is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This function is available on Windows NT Server 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll that ships with the RRAS redistributable exports the function as <b>RasAdminPortClearStats</b> rather than 
<b>MprAdminPortClearStats</b>. Therefore, when using the RRAS redistributable, use 
<a href="https://msdn.microsoft.com/en-us/library/ms684175(v=VS.85).aspx">LoadLibrary</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms683212(v=VS.85).aspx">GetProcAddress</a> to access this function.




## -see-also




<a href="https://msdn.microsoft.com/b6caa1f0-f4c7-48a9-b1e8-b484e7d7a3a3">MprAdminPortEnum</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

