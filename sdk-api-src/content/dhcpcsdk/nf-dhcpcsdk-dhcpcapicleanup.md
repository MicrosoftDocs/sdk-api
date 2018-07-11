---
UID: NF:dhcpcsdk.DhcpCApiCleanup
title: DhcpCApiCleanup function
author: windows-sdk-content
description: The DhcpCApiCleanup function enables DHCP to properly clean up resources allocated throughout the use of DHCP function calls. The DhcpCApiCleanup function must only be called if a previous call to DhcpCApiInitialize executed successfully.
old-location: dhcp\dhcpcapicleanup.htm
old-project: dhcp
ms.assetid: c1da731c-2e06-40ae-b104-25f144d50c36
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DhcpCApiCleanup, DhcpCApiCleanup function [DHCP], _dhcp_dhcpcapicleanup, dhcp.dhcpcapicleanup, dhcpcsdk/DhcpCApiCleanup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KSJACK_DESCRIPTION, *PKSJACK_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpCApiCleanup
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
---

# DhcpCApiCleanup function


## -description


The 
<b>DhcpCApiCleanup</b> function enables DHCP to properly clean up resources allocated throughout the use of DHCP function calls. The 
<b>DhcpCApiCleanup</b> function must only be called if a previous call to 
<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a> executed successfully.


## -parameters






## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a>
 

 

