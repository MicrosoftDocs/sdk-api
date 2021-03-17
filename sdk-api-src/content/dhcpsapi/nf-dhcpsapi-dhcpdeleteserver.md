---
UID: NF:dhcpsapi.DhcpDeleteServer
title: DhcpDeleteServer function (dhcpsapi.h)
description: The DhcpDeleteServer function attempts to delete a DHCP server and any related objects (such as subnet information and IP reservations) from the directory service.
helpviewer_keywords: ["DhcpDeleteServer","DhcpDeleteServer function [DHCP]","dhcp.dhcpdeleteserver","dhcpsapi/DhcpDeleteServer"]
old-location: dhcp\dhcpdeleteserver.htm
tech.root: DHCP
ms.assetid: 88b6c29b-7b01-40c7-b4f5-4920845f1eb9
ms.date: 12/05/2018
ms.keywords: DhcpDeleteServer, DhcpDeleteServer function [DHCP], dhcp.dhcpdeleteserver, dhcpsapi/DhcpDeleteServer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpDeleteServer
 - dhcpsapi/DhcpDeleteServer
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
 - DhcpDeleteServer
---

# DhcpDeleteServer function


## -description

The <b>DhcpDeleteServer</b> function attempts to delete a DHCP server and any related objects (such as subnet information and IP reservations) from the directory service.

## -parameters

### -param Flags [in]

Set to zero.

### -param IdInfo [in]

Set to null.

### -param NewServer [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpds_server">DHCP_SERVER_INFO</a> structure that contains the details of the DHCP server to delete from the directory service.

### -param CallbackFn [in]

Pointer to the function to call after this operation is executed. Set to null.

### -param CallbackData [in]

Pointer to the list of data that will be passed to the callback function specified in <i>CallbackFn</i>. Set to null.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpds_server">DHCP_SERVER_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumservers">DhcpEnumServers</a>