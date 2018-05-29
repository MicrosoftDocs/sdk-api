---
UID: NF:dhcpsapi.DhcpServerRedoAuthorization
title: DhcpServerRedoAuthorization function
author: windows-sdk-content
description: The DhcpServerRedoAuthorization function attempts to determine whether the DHCP server is authorized and restores leasing operations if it is not.
old-location: dhcp\dhcpserverredoauthorization.htm
old-project: DHCP
ms.assetid: c5bee9f1-7d4b-4dc2-a7c0-ebafd533ed50
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpServerRedoAuthorization, DhcpServerRedoAuthorization function [DHCP], dhcp.dhcpserverredoauthorization, dhcpsapi/DhcpServerRedoAuthorization
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpServerRedoAuthorization
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
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



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



An "authorized" DHCP server is a server currently leasing IP addresses for the subnets it has been set to administer. If a DHCP server has stopped leasing addresses, calling this method attempts to "redo" the authorization, and if <b>ERROR_SUCCESS</b> is returned, IP address leasing resumes.



