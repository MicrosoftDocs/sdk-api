---
UID: NF:dhcpsapi.DhcpEnumServers
title: DhcpEnumServers function
author: windows-driver-content
description: The DhcpEnumServers function returns an enumerated list of DHCP servers found in the directory service.
old-location: dhcp\dhcpenumservers.htm
old-project: DHCP
ms.assetid: c8b4d241-19d4-4a97-9129-c2954d63b6ac
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DhcpEnumServers, DhcpEnumServers function [DHCP], dhcp.dhcpenumservers, dhcpsapi/DhcpEnumServers
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpEnumServers
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
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

Pointer to a <a href="https://msdn.microsoft.com/0f5fe4f3-4eaa-498b-ab48-bfb5ee8f5527">DHCP_SERVER_INFO_ARRAY</a>
       structure that contains the output list of DHCP servers.


### -param CallbackFn [in]

Pointer to the callback function that will be called when the server add operation completes. This field should be null.


### -param CallbackData [in]

Pointer to a data block containing the formatted structure for callback information. This field should be null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f5fe4f3-4eaa-498b-ab48-bfb5ee8f5527">DHCP_SERVER_INFO_ARRAY</a>
 

 

