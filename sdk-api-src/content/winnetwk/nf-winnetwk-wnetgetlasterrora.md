---
UID: NF:winnetwk.WNetGetLastErrorA
title: WNetGetLastErrorA function (winnetwk.h)
description: The WNetGetLastError function retrieves the most recent extended error code set by a WNet function. The network provider reported this error code; it will not generally be one of the errors included in the SDK header file WinError.h. (ANSI)
helpviewer_keywords: ["WNetGetLastErrorA", "winnetwk/WNetGetLastErrorA"]
old-location: wnet\wnetgetlasterror.htm
tech.root: WNet
ms.assetid: 8e13c467-adcf-4e97-b51a-1f5fc919b51e
ms.date: 12/05/2018
ms.keywords: WNetGetLastError, WNetGetLastError function [Windows Networking (WNet)], WNetGetLastErrorA, WNetGetLastErrorW, _win32_wnetgetlasterror, winnetwk/WNetGetLastError, winnetwk/WNetGetLastErrorA, winnetwk/WNetGetLastErrorW, wnet.wnetgetlasterror
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetLastErrorW (Unicode) and WNetGetLastErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetGetLastErrorA
 - winnetwk/WNetGetLastErrorA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetGetLastError
 - WNetGetLastErrorA
 - WNetGetLastErrorW
---

# WNetGetLastErrorA function


## -description

The
				<b>WNetGetLastError</b> function retrieves the most recent extended error code set by a WNet function. The network provider reported this error code; it will not generally be one of the errors included in the SDK header file WinError.h.

## -parameters

### -param lpError [out]

Pointer to a variable that receives the error code reported by the network provider. The error code is specific to the network provider.

### -param lpErrorBuf [out]

Pointer to the buffer that receives the null-terminated string describing the error.

### -param nErrorBufSize [in]

Size of the buffer pointed to by the <i>lpErrorBuf</i> parameter, in characters. If the buffer is too small for the error string, the string is truncated but still null-terminated. A buffer of at least 256 characters is recommended.

### -param lpNameBuf [out]

Pointer to the buffer that receives the null-terminated string identifying the network provider that raised the error.

### -param nNameBufSize [in]

Size of the buffer pointed to by the <i>lpNameBuf</i> parameter, in characters. If the buffer is too small for the error string, the string is truncated but still null-terminated.

## -returns

If the function succeeds, and it obtains the last error that the network provider reported, the return value is NO_ERROR.

If the caller supplies an invalid buffer, the return value is ERROR_INVALID_ADDRESS.

## -remarks

The 
<b>WNetGetLastError</b> function retrieves errors that are specific to a network provider. You can call 
<b>WNetGetLastError</b> when a WNet function returns ERROR_EXTENDED_ERROR.

Like the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function, 
<b>WNetGetLastError</b> returns extended error information, which is maintained on a per-thread basis. Unlike <b>GetLastError</b>, the 
<b>WNetGetLastError</b> function can return a string for reporting errors that are not described by any existing error code in WinError.h.

For more information about using an application-defined error handler that calls the 
<b>WNetGetLastError</b> function, see 
<a href="/windows/desktop/WNet/retrieving-network-errors">Retrieving Network Errors</a>.





> [!NOTE]
> The winnetwk.h header defines WNetGetLastError as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
