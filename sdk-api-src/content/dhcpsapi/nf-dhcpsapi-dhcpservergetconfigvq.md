---
UID: NF:dhcpsapi.DhcpServerGetConfigVQ
title: DhcpServerGetConfigVQ function
author: windows-sdk-content
description: Retrieves the current DHCP server configuration settings.
old-location: dhcp\dhcpservergetconfigvq.htm
tech.root: DHCP
ms.assetid: 77726631-2be0-4ec0-a50f-786e4f3b460a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpServerGetConfigVQ, DhcpServerGetConfigVQ function [DHCP], dhcp.dhcpservergetconfigvq, dhcpsapi/DhcpServerGetConfigVQ
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpServerGetConfigVQ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpServerGetConfigVQ function


## -description


The <b>DhcpServerGetConfigVQ</b> function retrieves the current DHCP server configuration settings.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ConfigInfo [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a> structure that contains the returned DHCP server configuration settings.


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



The caller of this function must free the memory pointed to by <i>ConfigInfo</i> by calling <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a>



<a href="https://msdn.microsoft.com/3498b674-5771-47b6-9dfa-a8e3e10bca40">DhcpServerSetConfigVQ</a>
 

 

