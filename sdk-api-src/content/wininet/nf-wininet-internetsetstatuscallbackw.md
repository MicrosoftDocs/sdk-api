---
UID: NF:wininet.InternetSetStatusCallbackW
title: InternetSetStatusCallbackW
description: The InternetSetStatusCallbackW (Unicode) function sets up a callback function that WinINet functions can call as progress is made during an operation.
ms.date: 08/10/2022
ms.keywords: InternetSetStatusCallbackW
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wininet.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wininet.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - InternetSetStatusCallbackW
 - wininet/InternetSetStatusCallbackW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetStatusCallbackW
---

## -description

The InternetSetStatusCallback function sets up a callback function that WinINet functions can call as progress is made during an operation.

## -parameters

### -param hInternet

The handle for which the callback is set.

### -param lpfnInternetCallback

A pointer to the callback function to call when progress is made, or  <b>NULL</b> to remove the existing callback function. For more information about the callback function, see 
<a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a>.

## -returns

Returns the previously defined status callback function if successful, <b>NULL</b> if there was no previously defined status callback function, or INTERNET_INVALID_STATUS_CALLBACK if the callback function is not valid.

## -remarks

Both synchronous and asynchronous functions use the callback function to indicate the progress of the request, such as resolving a name, connecting to a server, and so on. The callback function is required for an asynchronous operation. The asynchronous request will call back to the application with INTERNET_STATUS_REQUEST_COMPLETE to indicate the request has been completed.

A callback function can be set on any handle, and is inherited by derived handles. A callback function can be changed using 
<b>InternetSetStatusCallback</b>, providing there are no pending requests that need to use the previous callback value. Note, however, that changing the callback function on a handle does not change the callbacks on derived handles, such as that returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>. You must change the callback function at each level.

Many of the WinINet functions perform several operations on the network. Each operation can take time to complete, and each can fail.

It is sometimes desirable to display status information during a long-term operation. You can display status information by setting up an Internet status callback function that cannot be removed as long as any callbacks or any asynchronous functions are pending.

After initiating 
<b>InternetSetStatusCallback</b>, the callback function can be accessed from within any WinINet function for monitoring time-intensive network operations.

<b>Note</b>  The callback function specified in the <i>lpfnInternetCallback</i> parameter will not be called on asynchronous operations for the request handle when the <i>dwContext</i> parameter of <a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> is set to zero (<b>INTERNET_NO_CALLBACK</b>), or the connection handle when the <i>dwContext</i> handle of <a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a> is set to zero (<b>INTERNET_NO_CALLBACK</b>).

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetSetStatusCallback as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>