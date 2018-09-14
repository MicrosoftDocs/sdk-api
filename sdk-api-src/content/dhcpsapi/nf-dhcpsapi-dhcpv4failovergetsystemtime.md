---
UID: NF:dhcpsapi.DhcpV4FailoverGetSystemTime
title: DhcpV4FailoverGetSystemTime function
author: windows-sdk-content
description: Returns the current time on the DHCP server.
old-location: dhcp\dhcpv4failovergetsystemtime.htm
tech.root: DHCP
ms.assetid: 3189e3d4-82cb-47a6-ad10-26a67c69e67d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DhcpV4FailoverGetSystemTime, DhcpV4FailoverGetSystemTime function [DHCP], dhcp.dhcpv4failovergetsystemtime, dhcpsapi/DhcpV4FailoverGetSystemTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4FailoverGetSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpV4FailoverGetSystemTime function


## -description


The <b>DhcpV4FailoverGetSystemTime</b> function returns the current time on the DHCP server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param pTime [out]

Pointer to a <b>DWORD</b> that returns the current time, in seconds, elapsed since midnight, January 1, 1970, Coordinated Universal Time (UTC), on the DHCP server. 


### -param pMaxAllowedDeltaTime

TBD




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
 



