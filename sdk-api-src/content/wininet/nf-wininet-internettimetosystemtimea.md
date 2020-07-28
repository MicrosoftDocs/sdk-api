---
UID: NF:wininet.InternetTimeToSystemTimeA
title: InternetTimeToSystemTimeA function (wininet.h)
description: Converts an HTTP time/date string to a SYSTEMTIME structure.
helpviewer_keywords: ["InternetTimeToSystemTime","InternetTimeToSystemTime function [WinINet]","InternetTimeToSystemTimeA","InternetTimeToSystemTimeW","_inet_internettimetosystemtime_function","wininet.internettimetosystemtime","wininet/InternetTimeToSystemTime","wininet/InternetTimeToSystemTimeA","wininet/InternetTimeToSystemTimeW"]
old-location: wininet\internettimetosystemtime.htm
tech.root: wininet
ms.assetid: fcfe99de-13b2-4e93-a978-f013ddae89f0
ms.date: 12/05/2018
ms.keywords: InternetTimeToSystemTime, InternetTimeToSystemTime function [WinINet], InternetTimeToSystemTimeA, InternetTimeToSystemTimeW, _inet_internettimetosystemtime_function, wininet.internettimetosystemtime, wininet/InternetTimeToSystemTime, wininet/InternetTimeToSystemTimeA, wininet/InternetTimeToSystemTimeW
f1_keywords:
- wininet/InternetTimeToSystemTime
dev_langs:
- c++
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetTimeToSystemTimeW (Unicode) and InternetTimeToSystemTimeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wininet.dll
- API-MS-Win-Http-Time-l1-1-0.dll
- KernelBase.dll
api_name:
- InternetTimeToSystemTime
- InternetTimeToSystemTimeA
- InternetTimeToSystemTimeW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetTimeToSystemTimeA function


## -description


Converts an HTTP time/date string to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.


## -parameters




### -param lpszTime [in]

Pointer to a null-terminated string that specifies the date/time to  be converted.


### -param pst [out]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the converted time.


### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if the string was converted, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetTimeToSystemTime as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

