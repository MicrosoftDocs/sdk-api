---
UID: NF:mprapi.MprConfigServerGetInfo
title: MprConfigServerGetInfo function
author: windows-sdk-content
description: The MprConfigServerGetInfo function retrieves server-level configuration information for the specified router.
old-location: rras\mprconfigservergetinfo.htm
old-project: rras
ms.assetid: 6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MprConfigServerGetInfo, MprConfigServerGetInfo function [RAS], _mpr_mprconfigservergetinfo, mprapi/MprConfigServerGetInfo, rras.mprconfigservergetinfo
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
 - MprConfigServerGetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigServerGetInfo function


## -description


The 
<b>MprConfigServerGetInfo</b> function retrieves server-level configuration information for the specified router.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, and 2 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>Windows 2000 Server or later: <a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows Server 2003 or later: <a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>Windows Server 2008 or later: <a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a>
</td>
</tr>
</table>
 


### -param lplpbBuffer [out]

On successful completion, a pointer to a 
<a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>, 
<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>,  
or   <a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free the memory for this buffer using 
<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




<ul>
<li>The <i>hMprConfig</i> parameter is <b>NULL</b>.</li>
<li>The <i>dwLevel</i> parameter is not zero.</li>
<li>The <i>lplpBuffer</i> parameter is <b>NULL</b>.</li>
</ul>
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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>



<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>



<a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a>



<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

