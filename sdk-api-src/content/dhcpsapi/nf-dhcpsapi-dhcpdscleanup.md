---
UID: NF:dhcpsapi.DhcpDsCleanup
title: DhcpDsCleanup function
author: windows-sdk-content
description: The DhcpDsCleanup function frees up directory service resources allocated for DHCP services by DhcpDsInit. This function should be called exactly once for each corresponding DHCP service process, and only when the process is terminated.
old-location: dhcp\dhcpdscleanup.htm
old-project: dhcp
ms.assetid: 7d722ca5-a779-4481-b2c7-6d9d7bb5fcfe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpDsCleanup, DhcpDsCleanup function [DHCP], dhcp.dhcpdscleanup, dhcpsapi/DhcpDsCleanup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpDsCleanup
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpDsCleanup function


## -description


The <b>DhcpDsCleanup</b> function frees up directory service resources allocated for DHCP services by <a href="https://msdn.microsoft.com/c622d492-91a8-4fd3-87ed-3545e7b83a0a">DhcpDsInit</a>. This function should be called exactly once for each corresponding DHCP service process, and only when the process is terminated. 


## -parameters






## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/c622d492-91a8-4fd3-87ed-3545e7b83a0a">DhcpDsInit</a>
 

 

