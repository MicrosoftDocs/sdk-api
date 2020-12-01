---
UID: NF:dhcpsapi.DhcpServerQueryAttribute
title: DhcpServerQueryAttribute function (dhcpsapi.h)
description: Returns specific attribute information from the DHCP server.
helpviewer_keywords: ["DhcpServerQueryAttribute","DhcpServerQueryAttribute function [DHCP]","dhcp.dhcpserverqueryattribute","dhcpsapi/DhcpServerQueryAttribute"]
old-location: dhcp\dhcpserverqueryattribute.htm
tech.root: DHCP
ms.assetid: 8a522a8d-0b65-4dce-a785-d2b0c70e2794
ms.date: 12/05/2018
ms.keywords: DhcpServerQueryAttribute, DhcpServerQueryAttribute function [DHCP], dhcp.dhcpserverqueryattribute, dhcpsapi/DhcpServerQueryAttribute
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DhcpServerQueryAttribute
 - dhcpsapi/DhcpServerQueryAttribute
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
 - DhcpServerQueryAttribute
---

# DhcpServerQueryAttribute function


## -description

The <b>DhcpServerQueryAttribute</b> function returns specific attribute information from the DHCP server.

## -parameters

### -param ServerIpAddr [in]

Unicode string that contains the IP address of the DHCP server.

### -param dwReserved [in]

Reserved. This value must be zero.

### -param DhcpAttribId [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_ATTRIB_ID</a> value that specifies the particular DHCP server attribute to retrieve.

### -param pDhcpAttrib [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_attrib">DHCP_ATTRIB</a> structure that contains the location and type of the queried DHCP server attribute.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

A DHCP server attribute is a value that can be queried to determine supported and available features.

Callers of this function should free the memory pointed to by <i>pDhcpAttrib</i> after use.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_attrib">DHCP_ATTRIB</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserverqueryattributes">DhcpServerQueryAttributes</a>