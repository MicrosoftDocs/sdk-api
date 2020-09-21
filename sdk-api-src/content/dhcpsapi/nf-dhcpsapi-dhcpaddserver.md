---
UID: NF:dhcpsapi.DhcpAddServer
title: DhcpAddServer function (dhcpsapi.h)
description: The DhcpAddServer function attempts to add a new server to the existing list of DHCP servers maintained in the domain directory service. If the specified DHCP server already exists in the directory service, an error is returned.
helpviewer_keywords: ["DhcpAddServer","DhcpAddServer function [DHCP]","dhcp.dhcpaddserver","dhcpsapi/DhcpAddServer"]
old-location: dhcp\dhcpaddserver.htm
tech.root: DHCP
ms.assetid: bdf5d239-478a-47af-9240-19d1b6933f7e
ms.date: 12/05/2018
ms.keywords: DhcpAddServer, DhcpAddServer function [DHCP], dhcp.dhcpaddserver, dhcpsapi/DhcpAddServer
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
 - DhcpAddServer
 - dhcpsapi/DhcpAddServer
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
 - DhcpAddServer
---

# DhcpAddServer function


## -description

The <b>DhcpAddServer</b> function attempts to add a new server to the existing list of DHCP servers maintained in the domain directory service. If the specified DHCP server  already exists in the directory service, an error is returned.

## -parameters

### -param Flags [in]

Reserved for future use. This field should be set to 0x00000000.

### -param IdInfo [in]

Pointer to an address containing the server's ID block. This field should be set to null.

### -param NewServer [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpds_server">DHCP_SERVER_INFO</a> structure containing information about the new DHCP server. The <b>DsLocation</b> and <b>DsLocType</b> members present in this structure are not valid in this implementation, and they should be set to null. The <b>Version</b> member of this structure should be set to 0.

### -param CallbackFn [in]

Pointer to the callback function that will be called when the server add operation completes. This field should be null.

### -param CallbackData [in]

Pointer to a data block containing the formatted structure for callback information. This field should be null.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpds_server">DHCP_SERVER_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeleteserver">DhcpDeleteServer</a>