---
UID: NF:dhcpsapi.DhcpSetThreadOptions
title: DhcpSetThreadOptions function (dhcpsapi.h)
description: The DhcpSetThreadOptions function sets options on the currently executing DHCP thread.
helpviewer_keywords: ["DHCP_FLAGS_DONT_ACCESS_DS","DhcpSetThreadOptions","DhcpSetThreadOptions function [DHCP]","dhcp.dhcpsetthreadoptions","dhcpsapi/DhcpSetThreadOptions"]
old-location: dhcp\dhcpsetthreadoptions.htm
tech.root: DHCP
ms.assetid: aadca143-6fdd-4b25-9bd5-1ba177be148e
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_DONT_ACCESS_DS, DhcpSetThreadOptions, DhcpSetThreadOptions function [DHCP], dhcp.dhcpsetthreadoptions, dhcpsapi/DhcpSetThreadOptions
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
 - DhcpSetThreadOptions
 - dhcpsapi/DhcpSetThreadOptions
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
 - DhcpSetThreadOptions
---

# DhcpSetThreadOptions function


## -description

The <b>DhcpSetThreadOptions</b> function sets options on the currently executing DHCP thread.

## -parameters

### -param Flags [in]

Set of bit flags indicating thread settings. If no thread options are  set, the value is 0. Currently, the only bit flag that can be set is as follows.

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
Do not access the directory service while the DHCP thread is executing. After this option is set, the only functions that can access the domain directory service are as follows:

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

### -param Reserved [in]

Reserved. This parameter must be set to <b>NULL</b>.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

<b>DhcpSetThreadOptions</b> currently allows only one option to be set.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetthreadoptions">DhcpGetThreadOptions</a>