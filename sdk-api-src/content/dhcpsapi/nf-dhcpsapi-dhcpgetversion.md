---
UID: NF:dhcpsapi.DhcpGetVersion
title: DhcpGetVersion function
author: windows-sdk-content
description: The DhcpGetVersion function returns the major and minor version numbers of the DHCP server.
old-location: dhcp\dhcpgetversion.htm
tech.root: DHCP
ms.assetid: 1977c4d7-094c-41b0-a7bf-aacdb15e265f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DhcpGetVersion, DhcpGetVersion function [DHCP], dhcp.dhcpgetversion, dhcpsapi/DhcpGetVersion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.



