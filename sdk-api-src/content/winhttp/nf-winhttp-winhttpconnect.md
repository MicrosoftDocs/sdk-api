---
UID: NF:winhttp.WinHttpConnect
title: WinHttpConnect function (winhttp.h)
description: The WinHttpConnect function specifies the initial target server of an HTTP request and returns an HINTERNET connection handle to an HTTP session for that initial target.
helpviewer_keywords: ["INTERNET_DEFAULT_HTTPS_PORT","INTERNET_DEFAULT_HTTP_PORT","INTERNET_DEFAULT_PORT","WinHttpConnect","WinHttpConnect function [WinHTTP]","http.winhttpconnect","winhttp.winhttpconnect","winhttp/WinHttpConnect"]
old-location: http\winhttpconnect.htm
tech.root: http
ms.assetid: afcdad8d-687e-4a1f-99d8-5d8be13825fa
ms.date: 12/05/2018
ms.keywords: INTERNET_DEFAULT_HTTPS_PORT, INTERNET_DEFAULT_HTTP_PORT, INTERNET_DEFAULT_PORT, WinHttpConnect, WinHttpConnect function [WinHTTP], http.winhttpconnect, winhttp.winhttpconnect, winhttp/WinHttpConnect
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
 - WinHttpConnect
 - winhttp/WinHttpConnect
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
 - WinHttpConnect
---

# WinHttpConnect function


## -description

The <b>WinHttpConnect</b> function specifies the initial target server of an HTTP request and returns an <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> connection handle to an HTTP session for that initial target.

## -parameters

### -param hSession [in]

Valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> WinHTTP session handle returned by a previous call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>.

### -param pswzServerName [in]

Pointer to a <b>null</b>-terminated string that contains the host name of an HTTP server. Alternately, the string can contain the IP address of the site as a string, for example, 10.0.1.45.
Note that WinHttp does not accept international host names without converting them first to <a href="/previous-versions/windows/internet-explorer/ie-developer/">Punycode</a>. For more information, see <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.

### -param nServerPort [in]

Unsigned integer that specifies the TCP/IP port on the server to which a connection is made.  This parameter can be any valid TCP/IP port number, or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_DEFAULT_HTTP_PORT"></a><a id="internet_default_http_port"></a><dl>
<dt><b>INTERNET_DEFAULT_HTTP_PORT</b></dt>
</dl>
</td>
<td width="60%">
Uses the default port for HTTP servers (port 80). 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_DEFAULT_HTTPS_PORT"></a><a id="internet_default_https_port"></a><dl>
<dt><b>INTERNET_DEFAULT_HTTPS_PORT</b></dt>
</dl>
</td>
<td width="60%">
Uses the default port for HTTPS servers (port 443).  Selecting this port does not automatically establish a secure connection.  You must still specify the use of secure transaction semantics by using the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WINHTTP_FLAG_SECURE</a> flag with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_DEFAULT_PORT"></a><a id="internet_default_port"></a><dl>
<dt><b>INTERNET_DEFAULT_PORT</b></dt>
</dl>
</td>
<td width="60%">
Uses port 80 for HTTP and port 443 for Secure Hypertext Transfer Protocol (HTTPS). 

</td>
</tr>
</table>

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

Returns a valid connection handle to the HTTP session if the connection is successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Codes</th>
<th>Description</th>
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
<dt><b>ERROR_WINHTTP_INVALID_URL</b></dt>
</dl>
</td>
<td width="60%">
The URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPERATION_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_UNRECOGNIZED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL scheme could not be recognized, or is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The WinHTTP function support is being shut down or unloaded.

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

After the calling application has finished using the 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<b>WinHttpConnect</b>, it must be closed using the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> function.

<b>WinHttpConnect</b> specifies the target HTTP server, however a response can come from another server if the request was redirected.  You can determine the URL of the server sending the response by calling 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> with the WINHTTP_OPTION_URL flag.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following example shows how to use secure transaction semantics to download a resource from an HTTPS server. The sample code initializes the Microsoft Windows HTTP Services (WinHTTP) application programming interface (API), selects a target HTTPS server, then opens and sends a request for this secure resource.  
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a> is used with the request handle to determine how much data is available for download, then 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a> is used to read that data.  This process repeats until the entire document has been retrieved and displayed.


```cpp

    DWORD dwSize = 0;
    DWORD dwDownloaded = 0;
    LPSTR pszOutBuffer;
    BOOL  bResults = FALSE;
    HINTERNET  hSession = NULL, 
               hConnect = NULL,
               hRequest = NULL;

    // Use WinHttpOpen to obtain a session handle.
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                            WINHTTP_NO_PROXY_NAME, 
                            WINHTTP_NO_PROXY_BYPASS, 0);

    // Specify an HTTP server.
    if (hSession)
        hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                                   INTERNET_DEFAULT_HTTPS_PORT, 0);

    // Create an HTTP request handle.
    if (hConnect)
        hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                       NULL, WINHTTP_NO_REFERER, 
                                       WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                       WINHTTP_FLAG_SECURE);

    // Send a request.
    if (hRequest)
        bResults = WinHttpSendRequest( hRequest,
                                       WINHTTP_NO_ADDITIONAL_HEADERS,
                                       0, WINHTTP_NO_REQUEST_DATA, 0, 
                                       0, 0);

 
    // End the request.
    if (bResults)
        bResults = WinHttpReceiveResponse( hRequest, NULL);

    // Keep checking for data until there is nothing left.
    if (bResults)
        do 
        {
            // Check for available data.
            dwSize = 0;
            if (!WinHttpQueryDataAvailable( hRequest, &dwSize))
                printf("Error %u in WinHttpQueryDataAvailable.\n", GetLastError());

            // Allocate space for the buffer.
            pszOutBuffer = new char[dwSize+1];
            if (!pszOutBuffer)
            {
                printf("Out of memory\n");
                dwSize=0;
            }
            else
            {
                // Read the Data.
                ZeroMemory(pszOutBuffer, dwSize+1);

                if (!WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                                      dwSize, &dwDownloaded))
                    printf( "Error %u in WinHttpReadData.\n", GetLastError());
                else
                    printf( "%s\n", pszOutBuffer);
            
                // Free the memory allocated to the buffer.
                delete [] pszOutBuffer;
            }

        } while (dwSize > 0);


    // Report any errors.
    if (!bResults)
        printf("Error %d has occurred.\n", GetLastError());

    // Close any open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>