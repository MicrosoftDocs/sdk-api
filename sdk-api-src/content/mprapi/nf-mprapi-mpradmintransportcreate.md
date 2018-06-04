---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MprAdminTransportCreate function


## -description


The 
<b>MprAdminTransportCreate</b> function loads a new transport, and starts the router manager for the transport.


## -parameters




### -param hMprServer [in]

Handle to the router on which to set the information. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport configuration type to set. Acceptable values for <i>dwTransportId</i> are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Transport (Protocol Family)</th>
</tr>
<tr>
<td>PID_ATALK</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>PID_IP</td>
<td>Internet Protocol version 4</td>
</tr>
<tr>
<td>PID_IPX</td>
<td>Internet Packet Exchange</td>
</tr>
<tr>
<td>PID_NBF</td>
<td>NetBIOS Frames Protocol</td>
</tr>
<tr>
<td>PID_IPV6</td>
<td>Windows Server 2008 or later: Internet Protocol version 6</td>
</tr>
</table>
 


### -param lpwsTransportName [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the transport.


### -param pGlobalInfo [in]

Pointer to a buffer that specifies global information for the transport. Use the 
<a href="https://msdn.microsoft.com/e88720aa-080b-4d87-a442-1b436c256ca6">Information Header Functions</a> to manipulate information headers.


### -param dwGlobalInfoSize [in]

Specifies the size, in bytes, of the data pointed to by the <i>pGlobalInfo</i> parameter.


### -param pClientInterfaceInfo [in, optional]

Pointer to a buffer that specifies default client interface information for the transport. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not set the default client interface information.


### -param dwClientInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the buffer pointed to by the <i>pClientInterfaceInfo</i> parameter.


### -param lpwsDLLPath [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the path to the DLL for the transport.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pGlobalInfo</i> parameter and the <i>pClientInterfaceInfo</i> parameter are both <b>NULL</b>.

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
<dt><b>ERROR_PROTOCOL_ALREADY_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The specified transport is already running on the specified router.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any supported transport protocol.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/47fbe483-8a1b-4747-9555-931dd63e2db8">MprAdminTransportGetInfo</a>



<a href="https://msdn.microsoft.com/ac0be570-e484-481b-9b16-ccdd4870deda">MprAdminTransportSetInfo</a>
 

 

