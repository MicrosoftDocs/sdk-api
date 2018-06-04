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

# DhcpV4GetAllOptionValues function


## -description


The <b>DhcpV4GetAllOptionValues</b> function retrieves an array of DHCP option values (the option code and associated data) for a particular scope. 


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param Flags [in]

Indicates whether the option values are for a specific or default vendor.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option values are retrieved for a default vendor.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option values are retrieved for specific vendors.

</td>
</tr>
</table>
 


### -param ScopeInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope of the option values to retrieve.


### -param Values [out]

Pointer to a <a href="https://msdn.microsoft.com/5b43263a-fea1-452b-9981-a0f2cf1c8cf0">DHCP_ALL_OPTION_VALUES_PB</a> structure that contains the retrieved option values for the scope specified in <i>ScopeInfo</i>.

There is one option value in the array for each vendor/policy pair defined on the DHCP server.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

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
One or more of the parameters were invalid.

</td>
</tr>
</table>
 




## -remarks



<i>Values</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/eadb26ec-50d5-474f-b6fe-1a586889bd23">DhcpV4GetOptionValue</a>



<a href="https://msdn.microsoft.com/9f22e44e-0eb8-48a9-8a82-dccf41535ef6">DhcpV4RemoveOptionValue</a>



<a href="https://msdn.microsoft.com/cf8141cc-8cf3-4932-b13a-e276dcdeb825">DhcpV4SetOptionValue</a>



<a href="https://msdn.microsoft.com/8c50af53-8298-401e-826e-0fb1d1410499">DhcpV4SetOptionValues</a>
 

 

