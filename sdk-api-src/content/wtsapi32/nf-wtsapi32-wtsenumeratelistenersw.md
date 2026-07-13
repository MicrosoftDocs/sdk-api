---
UID: NF:wtsapi32.WTSEnumerateListenersW
title: WTSEnumerateListenersW function (wtsapi32.h)
description: Enumerates all the Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["WTSEnumerateListeners", "WTSEnumerateListeners function [Remote Desktop Services]", "WTSEnumerateListenersW", "termserv.wtsenumeratelisteners", "wtsapi32/WTSEnumerateListeners", "wtsapi32/WTSEnumerateListenersW"]
old-location: termserv\wtsenumeratelisteners.htm
tech.root: TermServ
ms.assetid: dcdf4b4e-de01-4c23-97f6-0d45ba8608f5
ms.date: 12/05/2018
ms.keywords: WTSEnumerateListeners, WTSEnumerateListeners function [Remote Desktop Services], WTSEnumerateListenersA, WTSEnumerateListenersW, termserv.wtsenumeratelisteners, wtsapi32/WTSEnumerateListeners, wtsapi32/WTSEnumerateListenersA, wtsapi32/WTSEnumerateListenersW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateListenersW (Unicode) and WTSEnumerateListenersA (ANSI)
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
 - WTSEnumerateListenersW
 - wtsapi32/WTSEnumerateListenersW
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
 - WTSEnumerateListeners
 - WTSEnumerateListenersA
 - WTSEnumerateListenersW
---

# WTSEnumerateListenersW function


## -description

Enumerates all the Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to 
      <b>WTS_CURRENT_SERVER_HANDLE</b>.

### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.

### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.

### -param pListeners [out, optional]

A pointer to an array of <b>WTSLISTENERNAME</b> variables that receive the names of 
      the listeners.

### -param pCount [in, out]

A pointer to a <b>DWORD</b> variable that contains the number of listener names in 
      the array referenced by the <i>pListeners</i> parameter. If the number of listener names is 
      unknown, pass <i>pListeners</i> as <b>NULL</b>. The function will return 
      the number of  <b>WTSLISTENERNAME</b> variables necessary to allocate for the array 
      pointed to by the <i>pListeners</i> parameter.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function  returns all listeners currently running on the server, including listeners that do not support 
    Remote Desktop Protocol (RDP).

If the number of listeners is unknown, you can call this function with <i>pListeners</i> 
    set to <b>NULL</b>. The function will then return, in the <i>pCount</i> 
    parameter, the number of <b>WTSLISTENERNAME</b> variables necessary to receive all the 
    listeners. Allocate the array for <i>pListeners</i> based on this number, and then call the 
    function again, setting <i>pListeners</i> to the newly allocated array and 
    <i>pCount</i> to the number returned by the first call.




> [!NOTE]
> The wtsapi32.h header defines WTSEnumerateListeners as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
