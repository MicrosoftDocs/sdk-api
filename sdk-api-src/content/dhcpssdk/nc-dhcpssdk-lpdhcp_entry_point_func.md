---
UID: NC:dhcpssdk.LPDHCP_ENTRY_POINT_FUNC
title: LPDHCP_ENTRY_POINT_FUNC (dhcpssdk.h)
description: The DhcpServerCalloutEntry function is called by Microsoft DHCP Server to initialize a third-party DLL, and to discover for which events the third-party DLL wants notification. The DhcpServerCalloutEntry function is implemented by third-party DLLs.
helpviewer_keywords: ["DhcpServerCalloutEntry","LPDHCP_ENTRY_POINT_FUNC","LPDHCP_ENTRY_POINT_FUNC callback","LPDHCP_ENTRY_POINT_FUNC callback function [DHCP]","_dhcp_dhcpservercalloutentry","dhcp.dhcpservercalloutentry","dhcpssdk/LPDHCP_ENTRY_POINT_FUNC"]
old-location: dhcp\dhcpservercalloutentry.htm
tech.root: DHCP
ms.assetid: a80c2cd3-291d-4646-9dba-20a42e78dee5
ms.date: 12/05/2018
ms.keywords: DhcpServerCalloutEntry, LPDHCP_ENTRY_POINT_FUNC, LPDHCP_ENTRY_POINT_FUNC callback, LPDHCP_ENTRY_POINT_FUNC callback function [DHCP], _dhcp_dhcpservercalloutentry, dhcp.dhcpservercalloutentry, dhcpssdk/LPDHCP_ENTRY_POINT_FUNC
req.header: dhcpssdk.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDHCP_ENTRY_POINT_FUNC
 - dhcpssdk/LPDHCP_ENTRY_POINT_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - LPDHCP_ENTRY_POINT_FUNC
---

# LPDHCP_ENTRY_POINT_FUNC callback function


## -description

The 
<b>DhcpServerCalloutEntry</b> function is called by Microsoft DHCP Server to initialize a third-party DLL, and to discover for which events the third-party DLL wants notification. The 
<b>DhcpServerCalloutEntry</b> function is implemented by third-party DLLs.

## -parameters

### -param ChainDlls [in]

Collection of remaining third-party DLLs that provided registry entries requesting notification of DHCP Server events, in REG_MULTI_SZ format.

### -param CalloutVersion [in]

Version of the DHCP Server API that the third-party DLL is expected to support. The current version number is zero.

### -param CalloutTbl [out]

Cumulative set of notification hooks requested by all third-party DLLs, in the form of a 
<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a> structure.

## -returns

Return values are defined by the application providing the callback.

## -remarks

Upon successful loading of a third-party DLL, Microsoft DHCP Server calls the DLL's 
<b>DhcpServerCalloutEntry</b> function. If this function call succeeds, Microsoft DHCP Server does not attempt to load any further third-party DLLs, and instead passes the list of remaining third-party DLLs in the <i>ChainDlls</i> parameter. It is the responsibility of the loaded third-party DLL to ensure that:

<ul>
<li>other third-party DLLs are loaded</li>
<li>their 
<b>DhcpServerCalloutEntry</b> function called</li>
<li>the merged list of requested notification entry points are returned to Microsoft DHCP Server in the <i>CalloutTbl</i> parameter.</li>
</ul>
The initially loaded third-party DLL is responsible for maintaining a table of cumulative notification entry points, and upon notification of a particular event, must call all chained third-party DLLs before returning to Microsoft DHCP Server.

<div class="alert"><b>Note</b>  For version negotiation, Microsoft DHCP Server may call the 
<b>DhcpServerCalloutEntry</b> function until a compatible version is found.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/chaining-multiple-third-party-dlls">Chaining Multiple Third-Party DLLs</a>



<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a>



<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>