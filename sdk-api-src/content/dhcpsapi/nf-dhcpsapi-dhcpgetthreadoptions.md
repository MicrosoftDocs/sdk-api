---
UID: NF:dhcpsapi.DhcpGetThreadOptions
title: DhcpGetThreadOptions function
author: windows-sdk-content
description: The DhcpGetThreadOptions function retrieves the current thread options as set by DhcpSetThreadOptions.
old-location: dhcp\dhcpgetthreadoptions.htm
old-project: dhcp
ms.assetid: 2ba4b971-467c-47a6-8c4d-8e41b7874c80
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DHCP_FLAGS_DONT_ACCESS_DS, DhcpGetThreadOptions, DhcpGetThreadOptions function [DHCP], dhcp.dhcpgetthreadoptions, dhcpsapi/DhcpGetThreadOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
 - DhcpGetThreadOptions
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetThreadOptions function


## -description



      The <b>DhcpGetThreadOptions</b> function  retrieves the current thread options as set by <a href="https://msdn.microsoft.com/aadca143-6fdd-4b25-9bd5-1ba177be148e">DhcpSetThreadOptions</a>. 


## -parameters




### -param pFlags [out]

Set of bit flags as set by a previous call to <a href="https://msdn.microsoft.com/aadca143-6fdd-4b25-9bd5-1ba177be148e">DhcpSetThreadOptions</a>. If no thread options are  set, the return value is 0. Currently, the only bit flag that can be set is as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_DONT_ACCESS_DS"></a><a id="dhcp_flags_dont_access_ds"></a><dl>
<dt><b>DHCP_FLAGS_DONT_ACCESS_DS</b></dt>
</dl>
</td>
<td width="60%">
Do not access the directory service while the DHCP thread is executing. After this option is set, the only functions that can access the domain directory service are:

<ul>
<li>
<a href="https://msdn.microsoft.com/c8b4d241-19d4-4a97-9129-c2954d63b6ac">DhcpEnumServers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bdf5d239-478a-47af-9240-19d1b6933f7e">DhcpAddServer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/88b6c29b-7b01-40c7-b4f5-4920845f1eb9">DhcpDeleteServer</a>
</li>
</ul>
</td>
</tr>
</table>
 


### -param Reserved [out]

Reserved. This parameter must be set to null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/aadca143-6fdd-4b25-9bd5-1ba177be148e">DhcpSetThreadOptions</a>
 

 

