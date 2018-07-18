---
UID: NF:dhcpsapi.DhcpDsInit
title: DhcpDsInit function
author: windows-sdk-content
description: The DhcpDsInit function initializes memory within the directory service for a new DHCP server process.
old-location: dhcp\dhcpdsinit.htm
old-project: dhcp
ms.assetid: c622d492-91a8-4fd3-87ed-3545e7b83a0a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DhcpDsInit, DhcpDsInit function [DHCP], dhcp.dhcpdsinit, dhcpsapi/DhcpDsInit
ms.prod: windows
ms.technology: windows-sdk
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
 - DhcpDsInit
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpDsInit function


## -description



      The <b>DhcpDsInit</b> function initializes memory within the directory service for a new DHCP server process. 


## -parameters






## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function is called once per process. 




## -see-also




<a href="https://msdn.microsoft.com/7d722ca5-a779-4481-b2c7-6d9d7bb5fcfe">DhcpDsCleanup</a>
 

 

