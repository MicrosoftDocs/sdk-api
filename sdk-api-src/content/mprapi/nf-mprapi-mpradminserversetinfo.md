---
UID: NF:mprapi.MprAdminServerSetInfo
title: MprAdminServerSetInfo function
author: windows-driver-content
description: The MprAdminServerSetInfo function is used to set the number of ports for L2TP, PPTP, and SSTP devices when the RRAS service is running.
old-location: rras\mpradminserversetinfo.htm
old-project: RRAS
ms.assetid: 37187f6f-388e-47d6-83a8-92c2f69f71d9
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: MprAdminServerSetInfo, MprAdminServerSetInfo function [RAS], mprapi/MprAdminServerSetInfo, rras.mpradminserversetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	MprAdminServerSetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminServerSetInfo function


## -description


The 
<b>MprAdminServerSetInfo</b> function is used to set the number of ports for L2TP, PPTP, and SSTP  devices when the RRAS service is running. 



## -parameters




### -param hMprServer [in]

Handle to the router to query. Obtain this handle by calling <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>. 


### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 1 and 2 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
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
 


### -param lpbBuffer [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>  
or   <a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.


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
<dt><b>ERROR_SUCCESS_REBOOT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A system reboot is required for such a change to take affect. Change the port count using the <a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a> call and reboot.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
If you try to set the number of ports to more than the system supported limits as defined on the <a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a> and <a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a> topics.

Returns this error if you try to set the number of PPTP ports to 0.

Returns this error if the flags are not valid or if <i>lpbBuffer</i> or <i>hMprServer</i> is <b>NULL</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
RRAS service is not running on this server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwLevel</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hMprServer</i> handle is invalid.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



This function is used to set the port count for L2TP, PPTP, and SSTP ports and enable or disable RRAS when the service is running. These values are persistent, meaning that you do not have to follow this call with a call to <a href="https://msdn.microsoft.com/95fe0dfb-cfa6-4e84-a060-4b0fffc71a3d">MprConfigServerSetInfo</a>. Note that this function is asynchronous, so you might not see the affect of the changes immediately.


#### Examples

The topic <a href="https://msdn.microsoft.com/9e4aa8d4-e09e-4c84-acf0-c505a58841a4">Setting L2TP and PPTP ports of a local RRAS service</a> shows this function in use.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>



<a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a>



<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/d15dfb60-1239-4552-985f-d3c98f2981f4">MprAdminServerGetInfo</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

