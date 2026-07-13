---
UID: NF:wtsapi32.WTSOpenServerExA
title: WTSOpenServerExA function (wtsapi32.h)
description: Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server. (ANSI)
helpviewer_keywords: ["WTSOpenServerExA", "wtsapi32/WTSOpenServerExA"]
old-location: termserv\wtsopenserverex.htm
tech.root: TermServ
ms.assetid: 8122de66-c096-4bd8-95ff-ed64b88afcae
ms.date: 12/05/2018
ms.keywords: WTSOpenServerEx, WTSOpenServerEx function [Remote Desktop Services], WTSOpenServerExA, WTSOpenServerExW, termserv.wtsopenserverex, wtsapi32/WTSOpenServerEx, wtsapi32/WTSOpenServerExA, wtsapi32/WTSOpenServerExW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSOpenServerExW (Unicode) and WTSOpenServerExA (ANSI)
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
 - WTSOpenServerExA
 - wtsapi32/WTSOpenServerExA
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
 - WTSOpenServerEx
 - WTSOpenServerExA
 - WTSOpenServerExW
---

# WTSOpenServerExA function


## -description

Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.

## -parameters

### -param pServerName [in]

A pointer to a null-terminated string that contains the NetBIOS name of the server.

## -returns

If the function succeeds, the return value is a handle to the specified server.

If the function fails, it returns an invalid handle. You can test the validity of the handle by using it in another function call.

## -remarks

If the server specified by the <i>pServerName</i> parameter is an RD Session Host server, the behavior of this function is identical to  that of the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function.

To work with sessions running on virtual machines on the RD Virtualization Host server on which the calling application is running, specify <b>WTS_CURRENT_SERVER_NAME</b> for the <i>pServerName</i> parameter.

When you have finished using the handle returned by this function, release it by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtscloseserver">WTSCloseServer</a> function.





> [!NOTE]
> The wtsapi32.h header defines WTSOpenServerEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtscloseserver">WTSCloseServer</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>
