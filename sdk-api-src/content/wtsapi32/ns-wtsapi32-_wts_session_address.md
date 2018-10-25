---
UID: NS:wtsapi32._WTS_SESSION_ADDRESS
title: "_WTS_SESSION_ADDRESS"
author: windows-sdk-content
description: Contains the virtual IP address assigned to a session.
old-location: termserv\wts_session_address.htm
tech.root: termserv
ms.assetid: 4a8846a3-2bad-4ea1-b614-aca18484ea86
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PWTS_SESSION_ADDRESS, PWTS_SESSION_ADDRESS, PWTS_SESSION_ADDRESS structure pointer [Remote Desktop Services], WTS_SESSION_ADDRESS, WTS_SESSION_ADDRESS structure [Remote Desktop Services], _WTS_SESSION_ADDRESS, termserv.wts_session_address, wtsapi32/PWTS_SESSION_ADDRESS, wtsapi32/WTS_SESSION_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_SESSION_ADDRESS
product: Windows
targetos: Windows
req.typenames: WTS_SESSION_ADDRESS, *PWTS_SESSION_ADDRESS
req.redist: 
---

# _WTS_SESSION_ADDRESS structure


## -description


Contains the virtual IP address assigned to a session. This structure is returned by the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function when you specify "WTSSessionAddressV4" for the <i>WTSInfoClass</i> parameter.


## -struct-fields




### -field AddressFamily

A null-terminated string that contains the address family. Always set this member to "AF_INET".


### -field Address

The virtual IP address assigned to the session. The format of this address is identical to that used in the <a href="https://msdn.microsoft.com/29034986-f8d1-4cf0-9f53-e4b195d450a6">WTS_CLIENT_ADDRESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/29034986-f8d1-4cf0-9f53-e4b195d450a6">WTS_CLIENT_ADDRESS</a>
 

 

