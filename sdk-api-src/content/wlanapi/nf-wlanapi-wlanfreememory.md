---
UID: NF:wlanapi.WlanFreeMemory
title: WlanFreeMemory function (wlanapi.h)
description: Frees memory.
helpviewer_keywords: ["WlanFreeMemory","WlanFreeMemory function [NativeWIFI]","nwifi.wlanfreememory","wlanapi/WlanFreeMemory"]
old-location: nwifi\wlanfreememory.htm
tech.root: nwifi
ms.assetid: 241afb9d-8b16-4d76-b311-302b5492853e
ms.date: 12/05/2018
ms.keywords: WlanFreeMemory, WlanFreeMemory function [NativeWIFI], nwifi.wlanfreememory, wlanapi/WlanFreeMemory
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
 - WlanFreeMemory
 - wlanapi/WlanFreeMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanFreeMemory
---

# WlanFreeMemory function


## -description

The <b>WlanFreeMemory</b> function frees memory.  Any memory returned from Native Wifi functions must be freed.

## -parameters

### -param pMemory [in]

Pointer to the memory to be freed.

## -remarks

If <i>pMemory</i> points to memory that has already been freed, an access violation or heap corruption may occur.

There is a hotfix available for  Wireless LAN API for Windows XP with Service Pack 2 (SP2) that can help improve the performance of applications that call <b>WlanFreeMemory</b> and <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a> many times. 

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory">WlanAllocateMemory</a>