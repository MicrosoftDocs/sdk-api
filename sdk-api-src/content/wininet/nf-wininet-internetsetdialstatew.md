---
UID: NF:wininet.InternetSetDialStateW
title: InternetSetDialStateW function (wininet.h)
description: The InternetSetDialStateW (Unicode) function (wininet.h) is not supported, is obsolete, and should not be used.
helpviewer_keywords: ["InternetSetDialState", "InternetSetDialState function [WinINet]", "InternetSetDialStateW", "_inet_internetsetdialstate_function", "wininet.internetsetdialstate", "wininet/InternetSetDialState", "wininet/InternetSetDialStateW"]
old-location: wininet\internetsetdialstate.htm
tech.root: wininet
ms.assetid: f523f1ca-3e5a-4da0-850f-8654c82ee41e
ms.date: 08/10/2022
ms.keywords: InternetSetDialState, InternetSetDialState function [WinINet], InternetSetDialStateA, InternetSetDialStateW, _inet_internetsetdialstate_function, wininet.internetsetdialstate, wininet/InternetSetDialState, wininet/InternetSetDialStateA, wininet/InternetSetDialStateW, winineti/InternetSetDialState, winineti/InternetSetDialStateA, winineti/InternetSetDialStateW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetDialStateW (Unicode) and InternetSetDialStateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetSetDialStateW
 - wininet/InternetSetDialStateW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetDialState
 - InternetSetDialStateA
 - InternetSetDialStateW
---

# InternetSetDialStateW function


## -description

Not supported.

This function is obsolete. Do not use.

## -parameters

### -param lpszConnectoid

Unused.

### -param dwState

Unused.

### -param dwReserved

Unused.

## -returns

This function does not return a value.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



> [!NOTE]
> The wininet.h header defines InternetSetDialState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
