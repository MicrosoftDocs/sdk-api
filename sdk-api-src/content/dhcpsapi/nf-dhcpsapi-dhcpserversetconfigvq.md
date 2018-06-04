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

# DhcpServerSetConfigVQ function


## -description


The <b>DhcpServerSetConfigVQ</b> function sets or updates DHCP server settings.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param FieldsToSet [in]

Specifies a bitmask of the fields to set in the <a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a> structure passed to <i>ConfigInfo</i>.


### -param ConfigInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a> structure that contains the new or updated settings for the DHCP server.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
</table>
 




## -remarks



Most settings are effective immediately and do not require a restart.

The following DHCP server settings require a restart of the DHCP service:<ul>
<li>Set_APIProtocolSupport</li>
<li>Set_DatabaseName</li>
<li>Set_DatabasePath</li>
<li>Set_DatabaseLoggingPath</li>
<li>Set_RestoreFlag</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a>
 

 

