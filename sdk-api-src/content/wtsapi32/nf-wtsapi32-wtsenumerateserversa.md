---
UID: NF:wtsapi32.WTSEnumerateServersA
title: WTSEnumerateServersA function (wtsapi32.h)
description: Returns a list of all Remote Desktop Session Host (RD Session Host) servers within the specified domain. (ANSI)
helpviewer_keywords: ["WTSEnumerateServersA", "wtsapi32/WTSEnumerateServersA"]
old-location: termserv\wtsenumerateservers.htm
tech.root: TermServ
ms.assetid: 49aa3813-4e29-420e-9309-3ef9b11f1da7
ms.date: 12/05/2018
ms.keywords: WTSEnumerateServers, WTSEnumerateServers function [Remote Desktop Services], WTSEnumerateServersA, WTSEnumerateServersW, termserv.wtsenumerateservers, wtsapi32/WTSEnumerateServers, wtsapi32/WTSEnumerateServersA, wtsapi32/WTSEnumerateServersW
req.header: wtsapi32.h
req.include-header: 
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSEnumerateServersA
 - wtsapi32/WTSEnumerateServersA
dev_langs:
 - c++
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
---

# WTSEnumerateServersA function


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

Points to an array of <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_server_infoa">WTS_SERVER_INFO</a> 
      structures, which contains the returned results of the enumeration. After use, the memory used by this buffer 
      should be freed by calling <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a>.

### -param pCount

Pointer to a variable that receives the number of 
      <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_server_infoa">WTS_SERVER_INFO</a> structures returned in the 
      <i>ppServerInfo</i> buffer.

## -returns

If the function succeeds, the return value is a nonzero value.

 If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function will not work if NetBT is disabled.





> [!NOTE]
> The wtsapi32.h header defines WTSEnumerateServers as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_server_infoa">WTS_SERVER_INFO</a>
