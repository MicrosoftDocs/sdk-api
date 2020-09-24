---
UID: NF:dhcpsapi.DhcpGetThreadOptions
title: DhcpGetThreadOptions function (dhcpsapi.h)
description: The DhcpGetThreadOptions function retrieves the current thread options as set by DhcpSetThreadOptions.
helpviewer_keywords: ["DHCP_FLAGS_DONT_ACCESS_DS","DhcpGetThreadOptions","DhcpGetThreadOptions function [DHCP]","dhcp.dhcpgetthreadoptions","dhcpsapi/DhcpGetThreadOptions"]
old-location: dhcp\dhcpgetthreadoptions.htm
tech.root: DHCP
ms.assetid: 2ba4b971-467c-47a6-8c4d-8e41b7874c80
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_DONT_ACCESS_DS, DhcpGetThreadOptions, DhcpGetThreadOptions function [DHCP], dhcp.dhcpgetthreadoptions, dhcpsapi/DhcpGetThreadOptions
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpGetThreadOptions
 - dhcpsapi/DhcpGetThreadOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpGetThreadOptions
---

# DhcpGetThreadOptions function


## -description

The <b>DhcpGetThreadOptions</b> function  retrieves the current thread options as set by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetthreadoptions">DhcpSetThreadOptions</a>.

## -parameters

### -param pFlags [out]

Set of bit flags as set by a previous call to <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetthreadoptions">DhcpSetThreadOptions</a>. If no thread options are  set, the return value is 0. Currently, the only bit flag that can be set is as follows.

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
<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumservers">DhcpEnumServers</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddserver">DhcpAddServer</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeleteserver">DhcpDeleteServer</a>
</li>
</ul>
</td>
</tr>
</table>

### -param Reserved [out]

Reserved. This parameter must be set to null.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetthreadoptions">DhcpSetThreadOptions</a>