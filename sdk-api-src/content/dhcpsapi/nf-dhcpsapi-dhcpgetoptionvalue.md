---
UID: NF:dhcpsapi.DhcpGetOptionValue
title: DhcpGetOptionValue function
author: windows-sdk-content
description: The DhcpGetOptionValue function retrieves a DHCP option value (the option code and associated data) for a particular scope.
old-location: dhcp\dhcpgetoptionvalue.htm
old-project: dhcp
ms.assetid: 7dca800f-2427-44b1-bc92-f9db54de08a5
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DhcpGetOptionValue, DhcpGetOptionValue function [DHCP], dhcp.dhcpgetoptionvalue, dhcpsapi/DhcpGetOptionValue
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
 - DhcpGetOptionValue
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetOptionValue function


## -description



      The <b>DhcpGetOptionValue</b> function retrieves a DHCP option value (the option code and associated data) for a particular scope.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the code for the option value to retrieve.


### -param ScopeInfo [in]


<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope where the option value is set.


### -param OptionValue [out]


<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a> structure that contains the returned option code and data.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">
        DHCP_OPTION_VALUE</a>
 

 

