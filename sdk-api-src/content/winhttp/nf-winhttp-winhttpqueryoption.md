---
UID: NF:winhttp.WinHttpQueryOption
title: WinHttpQueryOption function (winhttp.h)
description: The WinHttpQueryOption function queries an Internet option on the specified handle.
helpviewer_keywords: ["WinHttpQueryOption","WinHttpQueryOption function [WinHTTP]","http.winhttpqueryoption","winhttp.winhttpqueryoption_function","winhttp/WinHttpQueryOption"]
old-location: http\winhttpqueryoption.htm
tech.root: http
ms.assetid: 47973eab-de70-47bf-9713-97b87a500cfa
ms.date: 12/05/2018
ms.keywords: WinHttpQueryOption, WinHttpQueryOption function [WinHTTP], http.winhttpqueryoption, winhttp.winhttpqueryoption_function, winhttp/WinHttpQueryOption
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpQueryOption
 - winhttp/WinHttpQueryOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpQueryOption
---

# WinHttpQueryOption function


## -description

The <b>WinHttpQueryOption</b> function queries an Internet option on the specified handle.

## -parameters

### -param hInternet [in]

An <b>HINTERNET</b> handle on which to query information. Note that this can be either a Session handle or a Request handle, depending on what option is being queried; see the  <a href="/windows/desktop/WinHttp/option-flags">Option Flags</a> topic to determine which handle is appropriate to use in querying a particular option.

### -param dwOption [in]

An unsigned long integer value that contains the Internet option to query. This can be one of the 
<a href="/windows/desktop/WinHttp/option-flags">Option Flags</a> values.

### -param lpBuffer [out]

A pointer to a buffer that receives the option setting. Strings returned by the 
<b>WinHttpQueryOption</b> function are globally allocated, so the calling application must globally free the string when it finishes using it. Setting this parameter to <b>NULL</b> causes this function to return <b>FALSE</b>.  Calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> then returns ERROR_INSUFFICIENT_BUFFER and 
<i>lpdwBufferLength</i>          contains the number of bytes required to hold the requested information.

### -param lpdwBufferLength [in, out]

A pointer to an unsigned long integer variable that contains the length of 
<i>lpBuffer</i>, in bytes. When the function returns, the variable receives the length of the data placed into 
<i>lpBuffer</i>. If 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter receives the number of bytes required to hold the requested information.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following:

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be carried out because the handle supplied is not in the correct state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_OPTION</b></dt>
</dl>
</td>
<td width="60%">
An invalid option value was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the ERROR_INVALID_PARAMETER if an option flag that is invalid for the specified handle type is passed to the 
<i>dwOption</i> parameter.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example demonstrates retrieving the connection 
                time-out value:


```cpp
    DWORD data;
    DWORD dwSize = sizeof(DWORD);

    // Use WinHttpOpen to obtain an HINTERNET handle.
    HINTERNET hSession = WinHttpOpen(L"A WinHTTP Example Program/1.0", 
                                    WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                                    WINHTTP_NO_PROXY_NAME, 
                                    WINHTTP_NO_PROXY_BYPASS, 0);
    if (hSession)
    {


        // Use WinHttpQueryOption to retrieve internet options.
        if (WinHttpQueryOption( hSession, 
                                WINHTTP_OPTION_CONNECT_TIMEOUT, 
                                &data, &dwSize))
        {
            printf("Connection timeout: %u ms\n\n",data);
        }
        else
        {
            printf( "Error %u in WinHttpQueryOption.\n", GetLastError());
        }        
        
        // When finished, release the HINTERNET handle.
        WinHttpCloseHandle(hSession);
    }
    else
    {
        printf("Error %u in WinHttpOpen.\n", GetLastError());
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/option-flags">Option Flags</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>