---
UID: NF:dhcpsapi.DhcpGetServerBindingInfo
title: DhcpGetServerBindingInfo function
author: windows-sdk-content
description: The DhcpGetServerBindingInfo function returns endpoint bindings set on the DHCP server.
old-location: dhcp\dhcpgetserverbindinginfo.htm
old-project: DHCP
ms.assetid: c0f5c9c1-d421-4977-aa26-1b8b7406802d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DHCP_ENDPOINT_FLAG_CANT_MODIFY, DhcpGetServerBindingInfo, DhcpGetServerBindingInfo function [DHCP], dhcp.dhcpgetserverbindinginfo, dhcpsapi/DhcpGetServerBindingInfo
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpGetServerBindingInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetServerBindingInfo function


## -description



      The <b>DhcpGetServerBindingInfo</b> function returns endpoint bindings set on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Specifies a set of flags describing the endpoints to return.

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
Returns unmodifiable endpoints only.

</td>
</tr>
</table>
 


### -param BindElementsInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/9e43b2ab-f69d-4024-b6b1-8a36a3577767">DHCP_BIND_ELEMENT_ARRAY</a> structure that contains the server network endpoint bindings.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires network byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/9e43b2ab-f69d-4024-b6b1-8a36a3577767">
        DHCP_BIND_ELEMENT_ARRAY</a>



<a href="https://msdn.microsoft.com/6291e266-e9d5-4899-8b34-53695f49a1b8">DhcpSetServerBindingInfo</a>
 

 

