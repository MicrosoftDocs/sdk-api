---
UID: NF:dhcpcsdk.DhcpCApiInitialize
title: DhcpCApiInitialize function
author: windows-driver-content
description: The DhcpCApiInitialize function must be the first function call made by users of DHCP; it prepares the system for all other DHCP function calls. Other DHCP functions should only be called if the DhcpCApiInitialize function executes successfully.
old-location: dhcp\dhcpcapiinitialize.htm
old-project: DHCP
ms.assetid: b4bc8b02-63b4-4751-a963-25336e8ae426
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: DhcpCApiInitialize, DhcpCApiInitialize function [DHCP], _dhcp_dhcpcapiinitialize, dhcp.dhcpcapiinitialize, dhcpcsdk/DhcpCApiInitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KSJACK_DESCRIPTION, *PKSJACK_DESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpcsvc.dll
api_name:
-	DhcpCApiInitialize
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
---

# DhcpCApiInitialize function


## -description


The 
<b>DhcpCApiInitialize</b> function must be the first function call made by users of DHCP; it prepares the system for all other DHCP function calls. Other DHCP functions should only be called if the 
<b>DhcpCApiInitialize</b> function executes successfully.


## -parameters




### -param Version [out]

Pointer to the DHCP version implemented by the client.


## -returns



Returns ERROR_SUCCESS upon successful completion.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/c1da731c-2e06-40ae-b104-25f144d50c36">DhcpCApiCleanup</a>
 

 

