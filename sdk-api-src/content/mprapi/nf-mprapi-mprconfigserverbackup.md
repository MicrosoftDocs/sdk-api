---
UID: NF:mprapi.MprConfigServerBackup
title: MprConfigServerBackup function
author: windows-sdk-content
description: The MprConfigServerBackup function creates a backup of the router-manager, interface, and phone-book configuration for the router.
old-location: rras\mprconfigserverbackup.htm
old-project: rras
ms.assetid: 7e318742-78ba-4eb4-818b-939688e79d54
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MprConfigServerBackup, MprConfigServerBackup function [RAS], _mpr_mprconfigserverbackup, mprapi/MprConfigServerBackup, rras.mprconfigserverbackup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigServerBackup
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigServerBackup function


## -description


The 
<b>MprConfigServerBackup</b> function creates a backup of the router-manager, interface, and phone-book configuration for the router.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param lpwsPath [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the path to the directory in which to write the backup files. This path should end with a trailing backslash.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hMprConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/1489ce8a-4f9d-4cf0-8729-b24e8c571557">MprConfigServerRestore</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

