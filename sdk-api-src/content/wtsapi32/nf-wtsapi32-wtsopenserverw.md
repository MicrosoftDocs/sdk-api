---
UID: NF:wtsapi32.WTSOpenServerW
title: WTSOpenServerW function (wtsapi32.h)
description: Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["WTSOpenServer", "WTSOpenServer function [Remote Desktop Services]", "WTSOpenServerW", "_win32_wtsopenserver", "termserv.wtsopenserver", "wtsapi32/WTSOpenServer", "wtsapi32/WTSOpenServerW"]
old-location: termserv\wtsopenserver.htm
tech.root: TermServ
ms.assetid: f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3
ms.date: 12/05/2018
ms.keywords: WTSOpenServer, WTSOpenServer function [Remote Desktop Services], WTSOpenServerA, WTSOpenServerW, _win32_wtsopenserver, termserv.wtsopenserver, wtsapi32/WTSOpenServer, wtsapi32/WTSOpenServerA, wtsapi32/WTSOpenServerW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSOpenServerW (Unicode) and WTSOpenServerA (ANSI)
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
 - WTSOpenServerW
 - wtsapi32/WTSOpenServerW
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
 - WTSOpenServer
 - WTSOpenServerA
 - WTSOpenServerW
---

# WTSOpenServerW function


## -description

Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param pServerName [in]

Pointer to a null-terminated string specifying the NetBIOS name of the RD Session Host server.

## -returns

If the function succeeds, the return value is a handle to the specified server.

If the function fails, it returns a handle that is not valid. You can test the validity of the handle by using it in another function call.

## -remarks

When you have finished using the handle returned by 
<b>WTSOpenServer</b>, release it by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtscloseserver">WTSCloseServer</a> function.

You do not need to open a handle for operations performed on the RD Session Host server on which your application is running. Use the constant <b>WTS_CURRENT_SERVER_HANDLE</b> instead.





> [!NOTE]
> The wtsapi32.h header defines WTSOpenServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtscloseserver">WTSCloseServer</a>
