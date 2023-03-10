---
UID: NS:wininet.INTERNET_ASYNC_RESULT
title: INTERNET_ASYNC_RESULT (wininet.h)
description: Contains the result of a call to an asynchronous function. This structure is used with InternetStatusCallback.
helpviewer_keywords: ["*LPINTERNET_ASYNC_RESULT","INTERNET_ASYNC_RESULT","INTERNET_ASYNC_RESULT structure [WinINet]","LPINTERNET_ASYNC_RESULT","LPINTERNET_ASYNC_RESULT structure pointer [WinINet]","_inet_internet_async_result_structure","wininet.internet_async_result","wininet/ LPINTERNET_ASYNC_RESULT","wininet/INTERNET_ASYNC_RESULT"]
old-location: wininet\internet_async_result.htm
tech.root: wininet
ms.assetid: e86fb4fd-8601-42e1-8c8e-9747a24459f9
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_ASYNC_RESULT, INTERNET_ASYNC_RESULT, INTERNET_ASYNC_RESULT structure [WinINet], LPINTERNET_ASYNC_RESULT, LPINTERNET_ASYNC_RESULT structure pointer [WinINet], _inet_internet_async_result_structure, wininet.internet_async_result, wininet/ LPINTERNET_ASYNC_RESULT, wininet/INTERNET_ASYNC_RESULT'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_ASYNC_RESULT, *LPINTERNET_ASYNC_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_ASYNC_RESULT
 - wininet/LPINTERNET_ASYNC_RESULT
 - INTERNET_ASYNC_RESULT
 - wininet/INTERNET_ASYNC_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_ASYNC_RESULT
---

# INTERNET_ASYNC_RESULT structure


## -description

Contains the result of a call to an asynchronous function. This structure is used with 
<a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a>.

## -struct-fields

### -field dwResult

Result. This parameter can be an 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle, unsigned long integer, or Boolean return code from an asynchronous function.

### -field dwError

Error code, if 
<b>dwResult</b> indicates that the function failed. If the operation succeeded, this member usually contains ERROR_SUCCESS.

## -remarks

The value of 
<b>dwResult</b> is determined by the value of  
<i>dwInternetStatus</i> in  the status callback function.
				


<table class="clsStd">
<tr>
<th>Value of 
<i>dwInternetStatus</i></th>
<th>Value of 
<b>dwResult</b></th>
</tr>
<tr>
<td>INTERNET_STATUS_HANDLE_CREATED</td>
<td>Pointer to the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle</td>
</tr>
<tr>
<td>INTERNET_STATUS_REQUEST_COMPLETE</td>
<td>Boolean return code from the asynchronous function.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/asynchronous-operation"> Asynchronous Operation</a>

