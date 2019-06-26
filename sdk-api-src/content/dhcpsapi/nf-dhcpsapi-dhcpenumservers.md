---
UID: NF:dhcpsapi.DhcpEnumServers
title: DhcpEnumServers function (dhcpsapi.h)
author: windows-sdk-content
description: The DhcpEnumServers function returns an enumerated list of DHCP servers found in the directory service.
old-location: dhcp\dhcpenumservers.htm
tech.root: DHCP
ms.assetid: c8b4d241-19d4-4a97-9129-c2954d63b6ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpEnumServers, DhcpEnumServers function [DHCP], dhcp.dhcpenumservers, dhcpsapi/DhcpEnumServers
ms.topic: function
f1_keywords: 
 - "dhcpsapi/DhcpEnumServers"
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
 - DhcpEnumServers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpEnumServers function


## -description


The <b>DhcpEnumServers</b> function returns an enumerated list of DHCP servers found in the directory service.  


## -parameters




### -param Flags [in]

Reserved for future use. This field should be set to 0.


### -param IdInfo [in]

Pointer to an address containing the server's ID block. This field should be set to null.


### -param Servers [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcpds_servers">DHCP_SERVER_INFO_ARRAY</a>structure that contains the output list of DHCP servers.


### -param CallbackFn [in]

Pointer to the callback function that will be called when the server add operation completes. This field should be null.


### -param CallbackData [in]

Pointer to a data block containing the formatted structure for callback information. This field should be null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcpds_servers">DHCP_SERVER_INFO_ARRAY</a>
 

 

