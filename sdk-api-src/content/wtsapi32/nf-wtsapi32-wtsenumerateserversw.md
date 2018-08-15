---
UID: NF:wtsapi32.WTSEnumerateServersW
title: WTSEnumerateServersW function
author: windows-sdk-content
description: Returns a list of all Remote Desktop Session Host (RD Session Host) servers within the specified domain.
old-location: termserv\wtsenumerateservers.htm
old-project: termserv
ms.assetid: 49aa3813-4e29-420e-9309-3ef9b11f1da7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WTSEnumerateServers, WTSEnumerateServers function [Remote Desktop Services], WTSEnumerateServersA, WTSEnumerateServersW, termserv.wtsenumerateservers, wtsapi32/WTSEnumerateServers, wtsapi32/WTSEnumerateServersA, wtsapi32/WTSEnumerateServersW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateServersW (Unicode) and WTSEnumerateServersA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSEnumerateServers
 - WTSEnumerateServersA
 - WTSEnumerateServersW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSEnumerateServersW function


## -description


Returns 
   a list of all Remote Desktop Session Host (RD Session Host) servers within the specified domain.


## -parameters




### -param pDomainName [in]

Pointer to the name of the domain to be queried. If the value of this parameter is 
      <b>NULL</b>, the specified domain is the current domain.


### -param Reserved [in]

Reserved. The value of this parameter must be 0.


### -param Version [in]

Version of the enumeration request. The value of the parameter must be 1.


### -param ppServerInfo

Points to an array of <a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a> 
      structures, which contains the returned results of the enumeration. After use, the memory used by this buffer 
      should be freed by calling <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>.


### -param pCount

Pointer to a variable that receives the number of 
      <a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a> structures returned in the 
      <i>ppServerInfo</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

 If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function will not work if NetBT is disabled.




## -see-also




<a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a>
 

 

