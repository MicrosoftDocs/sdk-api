---
UID: NF:dhcpsapi.DhcpServerRedoAuthorization
title: DhcpServerRedoAuthorization function (dhcpsapi.h)
description: The DhcpServerRedoAuthorization function attempts to determine whether the DHCP server is authorized and restores leasing operations if it is not.
helpviewer_keywords: ["DhcpServerRedoAuthorization","DhcpServerRedoAuthorization function [DHCP]","dhcp.dhcpserverredoauthorization","dhcpsapi/DhcpServerRedoAuthorization"]
old-location: dhcp\dhcpserverredoauthorization.htm
tech.root: DHCP
ms.assetid: c5bee9f1-7d4b-4dc2-a7c0-ebafd533ed50
ms.date: 12/05/2018
ms.keywords: DhcpServerRedoAuthorization, DhcpServerRedoAuthorization function [DHCP], dhcp.dhcpserverredoauthorization, dhcpsapi/DhcpServerRedoAuthorization
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
 - DhcpServerRedoAuthorization
 - dhcpsapi/DhcpServerRedoAuthorization
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
 - DhcpServerRedoAuthorization
---

# DhcpServerRedoAuthorization function


## -description

The <b>DhcpServerRedoAuthorization</b> function attempts to determine whether the DHCP server is authorized and restores leasing operations if it is not.

## -parameters

### -param ServerIpAddr [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param dwReserved [in]

Reserved. This parameter should be set to 0.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

An "authorized" DHCP server is a server currently leasing IP addresses for the subnets it has been set to administer. If a DHCP server has stopped leasing addresses, calling this method attempts to "redo" the authorization, and if <b>ERROR_SUCCESS</b> is returned, IP address leasing resumes.