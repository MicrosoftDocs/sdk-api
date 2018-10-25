---
UID: NF:mprapi.MprAdminInterfaceGetInfo
title: MprAdminInterfaceGetInfo function
author: windows-sdk-content
description: The MprAdminInterfaceGetInfo function retrieves information for a specified interface on a specified server.
old-location: rras\mpradmininterfacegetinfo.htm
tech.root: rras
ms.assetid: a6d353f0-1d68-4a37-89f3-cdab0fc7972a
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: MprAdminInterfaceGetInfo, MprAdminInterfaceGetInfo function [RAS], _mpr_mpradmininterfacegetinfo, mprapi/MprAdminInterfaceGetInfo, rras.mpradmininterfacegetinfo
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
 - MprAdminInterfaceGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminInterfaceGetInfo function


## -description


The 
<b>MprAdminInterfaceGetInfo</b> function retrieves information for a specified interface on a specified server.


## -parameters




### -param hMprServer [in]

Handle to the  router to query. This handle is obtained from a previous call to 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>. 


### -param hInterface [in]

Handle to the interface obtained by a previous call to 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lplpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>Windows Server 2008 or later: <a href="https://msdn.microsoft.com/d761a9cf-7b56-48ad-b98b-60fc99d0d8ba">MPR_INTERFACE_3</a>
</td>
</tr>
</table>
 

Values of 1, 2, and 3 are valid only for interfaces of type <a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a>.


### -param lplpbBuffer [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>, 
<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>,  
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a>, or  <a href="https://msdn.microsoft.com/d761a9cf-7b56-48ad-b98b-60fc99d0d8ba">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free this memory by calling 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> is  2, but that level is not supported for the interface. For example, the type of interface, as defined in the MPR_INTERFACE_X structure,  is not <b>IF_TYPE_FULL_ROUTER</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid.

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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> value is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>



<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>



<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a>



<a href="https://msdn.microsoft.com/d761a9cf-7b56-48ad-b98b-60fc99d0d8ba">MPR_INTERFACE_3</a>



<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

