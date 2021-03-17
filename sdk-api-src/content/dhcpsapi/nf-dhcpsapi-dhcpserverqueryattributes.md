---
UID: NF:dhcpsapi.DhcpServerQueryAttributes
title: DhcpServerQueryAttributes function (dhcpsapi.h)
description: Returns an array of attributes set on the DHCP server.
helpviewer_keywords: ["DhcpServerQueryAttributes","DhcpServerQueryAttributes function [DHCP]","dhcp.dhcpserverqueryattributes","dhcpsapi/DhcpServerQueryAttributes"]
old-location: dhcp\dhcpserverqueryattributes.htm
tech.root: DHCP
ms.assetid: 24c3e7b2-80eb-4fee-aea6-38243d25c50b
ms.date: 12/05/2018
ms.keywords: DhcpServerQueryAttributes, DhcpServerQueryAttributes function [DHCP], dhcp.dhcpserverqueryattributes, dhcpsapi/DhcpServerQueryAttributes
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
 - DhcpServerQueryAttributes
 - dhcpsapi/DhcpServerQueryAttributes
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
 - DhcpServerQueryAttributes
---

# DhcpServerQueryAttributes function


## -description

The <b>DhcpServerQueryAttributes</b> function returns an array of attributes set on the DHCP server.

## -parameters

### -param ServerIpAddr [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param dwReserved [in]

Reserved. This value must be set to zero.

### -param dwAttribCount [in]

Specifies the number of attributes listed in <i>pDhcpAttribArr</i>.

### -param pDhcpAttribs [in]

Specifies an array of <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_ATTRIB_ID</a> values (of length <i>dwAttribCount</i>) to retrieve the corresponding attribute information from.

### -param pDhcpAttribArr [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_attrib_array">DHCP_ATTRIB_ARRAY</a> structure that contains the attributes directly corresponding to the attribute ID values specified in <i>pDhcpAttribs[]</i>.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

A DHCP server attribute is a value that can be queried to determine supported and available features.

Callers of this function should free the memory pointed to by <i>pDhcpAttribs</i> and <i>pDhcpAttribArr</i> after use.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_attrib_array">DHCP_ATTRIB_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserverqueryattribute">DhcpServerQueryAttribute</a>