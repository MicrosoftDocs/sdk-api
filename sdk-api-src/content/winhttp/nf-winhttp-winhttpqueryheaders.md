---
UID: NF:winhttp.WinHttpQueryHeaders
title: WinHttpQueryHeaders function (winhttp.h)
description: The WinHttpQueryHeaders function retrieves header information associated with an HTTP request.
helpviewer_keywords: ["WinHttpQueryHeaders","WinHttpQueryHeaders function [WinHTTP]","http.winhttpqueryheaders","winhttp.winhttpqueryheaders_function","winhttp/WinHttpQueryHeaders"]
old-location: http\winhttpqueryheaders.htm
tech.root: http
ms.assetid: 9656ebad-78df-4d1c-94e9-6127d6bc4799
ms.date: 12/05/2018
ms.keywords: WinHttpQueryHeaders, WinHttpQueryHeaders function [WinHTTP], http.winhttpqueryheaders, winhttp.winhttpqueryheaders_function, winhttp/WinHttpQueryHeaders
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
 - WinHttpQueryHeaders
 - winhttp/WinHttpQueryHeaders
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
 - WinHttpQueryHeaders
---

## -description

The <b>WinHttpQueryHeaders</b> function retrieves header information associated with an HTTP request.

Also see [WinHttpQueryHeadersEx](nf-winhttp-winhttpqueryheadersex.md), which offers a way to retrieve parsed header name and value strings.

## -parameters

### -param hRequest [in]

<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> request handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>. 
WinHttpReceiveResponse must have been called for this handle and have completed before <b>WinHttpQueryHeaders</b> is called.

### -param dwInfoLevel [in]

Value of type <b>DWORD</b> that specifies a combination of attribute and modifier flags listed on the 
<a href="/windows/desktop/WinHttp/query-info-flags">Query Info Flags</a> page. These attribute and modifier flags indicate that the information is being requested and how it is to be formatted.

### -param pwszName [in, optional]

Pointer to a string that contains the header name. If the flag in 
<i>dwInfoLevel</i> is not 
<b>WINHTTP_QUERY_CUSTOM</b>, set this parameter to WINHTTP_HEADER_NAME_BY_INDEX.

### -param lpBuffer [out]

Pointer to the buffer that receives the information. Setting this parameter to WINHTTP_NO_OUTPUT_BUFFER causes this function to return <b>FALSE</b>.  Calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> then returns 
<b>ERROR_INSUFFICIENT_BUFFER</b> and 
<i>lpdwBufferLength</i> contains the number of bytes required to hold the requested information.

### -param lpdwBufferLength [in, out]

Pointer to a value of type <b>DWORD</b> that specifies the length of the data buffer, in bytes. When the function returns, this parameter contains the pointer to a value that specifies the length of the information written to the buffer. When the function returns strings, the following rules apply. 
					

<ul>
<li>If the function succeeds, 
<i>lpdwBufferLength</i> specifies the length of the string, in bytes, minus 2 for the terminating null. </li>
<li>If the function fails and 
<b>ERROR_INSUFFICIENT_BUFFER</b> is returned, 
<i>lpdwBufferLength</i> specifies the number of bytes that the application must allocate to receive the string. </li>
</ul>

### -param lpdwIndex [in, out]

Pointer to a zero-based header index used to enumerate multiple headers with the same name. When calling the function, this parameter is the index of the specified header to return. When the function returns, this parameter is the index of the next header. If the next index cannot be found, 
<b>ERROR_WINHTTP_HEADER_NOT_FOUND</b> is returned. Set this parameter to WINHTTP_NO_HEADER_INDEX to specify that only the first occurrence of a header should be returned.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_HEADER_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested header could not be located.

</td>
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

By default 
<b>WinHttpQueryHeaders</b> returns a string.  However, you can request data in the form of a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure or <b>DWORD</b> by including the appropriate modifier flag in 
<i>dwInfoLevel</i>.  The following table shows the possible data types that 
<b>WinHttpQueryHeaders</b> can return along with the modifier flag that you use to select that data type.

                


<table class="clsStd">
<tr>
<th>Data type</th>
<th>Modifier flag</th>
</tr>
<tr>
<td><b>LPCWSTR</b></td>
<td>Default.  No modifier flag required.</td>
</tr>
<tr>
<td><b>SYSTEMTIME</b></td>
<td><b>WINHTTP_QUERY_FLAG_SYSTEMTIME</b></td>
</tr>
<tr>
<td><b>DWORD</b></td>
<td><b>WINHTTP_QUERY_FLAG_NUMBER</b></td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following example shows how to obtain an 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle, open an HTTP session, create and send a request header, and examine the returned response header.


```cpp
    DWORD dwSize = 0;
    LPVOID lpOutBuffer = NULL;
    BOOL  bResults = FALSE;
    HINTERNET hSession = NULL,
              hConnect = NULL,
              hRequest = NULL;

    // Use WinHttpOpen to obtain a session handle.
    hSession = WinHttpOpen(  L"A WinHTTP Example Program/1.0",
                             WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                             WINHTTP_NO_PROXY_NAME,
                             WINHTTP_NO_PROXY_BYPASS, 0);

    // Specify an HTTP server.
    if (hSession)
        hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                                   INTERNET_DEFAULT_HTTP_PORT, 0);

    // Create an HTTP request handle.
    if (hConnect)
        hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                       NULL, WINHTTP_NO_REFERER,
                                       WINHTTP_DEFAULT_ACCEPT_TYPES,
                                       0);

    // Send a request.
    if (hRequest)
        bResults = WinHttpSendRequest( hRequest,
                                       WINHTTP_NO_ADDITIONAL_HEADERS,
                                       0, WINHTTP_NO_REQUEST_DATA, 0,
                                       0, 0);

    // End the request.
    if (bResults)
        bResults = WinHttpReceiveResponse( hRequest, NULL);

    // First, use WinHttpQueryHeaders to obtain the size of the buffer.
    if (bResults)
    {
        WinHttpQueryHeaders( hRequest, WINHTTP_QUERY_RAW_HEADERS_CRLF,
                             WINHTTP_HEADER_NAME_BY_INDEX, NULL,
                             &dwSize, WINHTTP_NO_HEADER_INDEX);

        // Allocate memory for the buffer.
        if( GetLastError( ) == ERROR_INSUFFICIENT_BUFFER )
        {
            lpOutBuffer = new WCHAR[dwSize/sizeof(WCHAR)];

            // Now, use WinHttpQueryHeaders to retrieve the header.
            bResults = WinHttpQueryHeaders( hRequest,
                                       WINHTTP_QUERY_RAW_HEADERS_CRLF,
                                       WINHTTP_HEADER_NAME_BY_INDEX,
                                       lpOutBuffer, &dwSize,
                                       WINHTTP_NO_HEADER_INDEX);
        }
    }

    // Print the header contents.
    if (bResults)
        printf("Header contents: \n%S",lpOutBuffer);

    // Free the allocated memory.
    delete [] lpOutBuffer;

    // Report any errors.
    if (!bResults)
        printf("Error %d has occurred.\n",GetLastError());

    // Close any open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



Microsoft Windows HTTP Services (WinHTTP)



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>