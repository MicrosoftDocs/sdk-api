---
UID: NF:wlanapi.WlanAllocateMemory
title: WlanAllocateMemory function (wlanapi.h)
description: Allocates memory.
helpviewer_keywords: ["WlanAllocateMemory","WlanAllocateMemory function [NativeWIFI]","nwifi.wlanallocatememory","wlanapi/WlanAllocateMemory"]
old-location: nwifi\wlanallocatememory.htm
tech.root: nwifi
ms.assetid: 29200450-4ec8-418d-b633-1ea688755711
ms.date: 12/05/2018
ms.keywords: WlanAllocateMemory, WlanAllocateMemory function [NativeWIFI], nwifi.wlanallocatememory, wlanapi/WlanAllocateMemory
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanAllocateMemory
 - wlanapi/WlanAllocateMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanAllocateMemory
---

# WlanAllocateMemory function


## -description

The <b>WlanAllocateMemory</b> function allocates memory.  Any memory passed to other Native Wifi functions must be allocated with this function.

## -parameters

### -param dwMemorySize [in]

Amount of  memory being requested, in bytes.

## -returns

If the call is successful, the function returns a pointer to the allocated memory.

If the memory could not be allocated for any reason or if the <i>dwMemorySize</i> parameter is 0, the returned pointer is <b>NULL</b>.

An application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain extended error information.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>