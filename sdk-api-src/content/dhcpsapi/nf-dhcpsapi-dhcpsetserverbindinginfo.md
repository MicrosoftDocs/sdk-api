---
UID: NF:dhcpsapi.DhcpSetServerBindingInfo
title: DhcpSetServerBindingInfo function
author: windows-sdk-content
description: The DhcpSetServerBindingInfo function sets endpoint bindings for the DHCP server.
old-location: dhcp\dhcpsetserverbindinginfo.htm
old-project: dhcp
ms.assetid: 6291e266-e9d5-4899-8b34-53695f49a1b8
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DHCP_ENDPOINT_FLAG_CANT_MODIFY, DhcpSetServerBindingInfo, DhcpSetServerBindingInfo function [DHCP], dhcp.dhcpsetserverbindinginfo, dhcpsapi/DhcpSetServerBindingInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
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
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpSetServerBindingInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetServerBindingInfo function


## -description



      The <b>DhcpSetServerBindingInfo</b> function sets endpoint bindings for the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Specifies a set of flags describing endpoint properties.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ENDPOINT_FLAG_CANT_MODIFY"></a><a id="dhcp_endpoint_flag_cant_modify"></a><dl>
<dt><b>DHCP_ENDPOINT_FLAG_CANT_MODIFY</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The endpoints cannot be modified.

</td>
</tr>
</table>
 


### -param BindElementInfo [in]


<a href="https://msdn.microsoft.com/9e43b2ab-f69d-4024-b6b1-8a36a3577767">DHCP_BIND_ELEMENT_ARRAY</a> structure that contains the endpoint bindings for the DHCP server.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires network byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/9e43b2ab-f69d-4024-b6b1-8a36a3577767">
        DHCP_BIND_ELEMENT_ARRAY</a>



<a href="https://msdn.microsoft.com/c0f5c9c1-d421-4977-aa26-1b8b7406802d">DhcpGetServerBindingInfo</a>
 

 

