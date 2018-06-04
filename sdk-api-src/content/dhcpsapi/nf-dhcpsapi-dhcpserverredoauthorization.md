---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



