---
UID: NF:dhcpsapi.DhcpGetVersion
title: DhcpGetVersion function (dhcpsapi.h)

description: The DhcpGetVersion function returns the major and minor version numbers of the DHCP server.
old-location: dhcp\dhcpgetversion.htm
tech.root: DHCP
ms.assetid: 1977c4d7-094c-41b0-a7bf-aacdb15e265f

ms.date: 12/05/2018
ms.keywords: DhcpGetVersion, DhcpGetVersion function [DHCP], dhcp.dhcpgetversion, dhcpsapi/DhcpGetVersion
ms.topic: function
f1_keywords: 
 - "dhcpsapi/DhcpGetVersion"
dev_langs:
 - c++
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
 - DhcpGetVersion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpGetVersion function


## -description


The <b>DhcpGetVersion</b> function returns the major and minor version numbers of the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param MajorVersion [out]

Specifies the major version number of the DHCP server.


### -param MinorVersion [out]

Specifies the minor version number of the DHCP server.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.



