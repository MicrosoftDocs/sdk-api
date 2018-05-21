---
UID: NF:mprapi.MprAdminServerGetInfo
title: MprAdminServerGetInfo function
author: windows-driver-content
description: The MprAdminServerGetInfo function retrieves information about the specified RRAS server.
old-location: rras\mpradminservergetinfo.htm
old-project: RRAS
ms.assetid: d15dfb60-1239-4552-985f-d3c98f2981f4
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: MprAdminServerGetInfo, MprAdminServerGetInfo function [RAS], _mpr_mpradminservergetinfo, mprapi/MprAdminServerGetInfo, rras.mpradminservergetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminServerGetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminServerGetInfo function


## -description


The 
<b>MprAdminServerGetInfo</b> function retrieves information about the specified RRAS server.


## -parameters




### -param hMprServer [in]

Handle to the router to query. Obtain this handle by calling <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


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
 


### -param lplpbBuffer

TBD




#### - lplpBuffer [out]

On successful completion, a pointer to a 
<a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>, 
<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>,  
or   <a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free the memory for this buffer using 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpbBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The <i>hMprServer</i> parameter is <b>NULL</b>. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cffda25b-28f8-4d76-987c-eadcea9c032b">MPR_SERVER_0</a>



<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>



<a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a>



<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminServerSetInfo</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

