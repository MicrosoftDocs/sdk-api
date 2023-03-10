---
UID: NF:winhttp.WinHttpQueryDataAvailable
title: WinHttpQueryDataAvailable function (winhttp.h)
description: Returns the amount of data, in bytes, available to be read with WinHttpReadData.
helpviewer_keywords: ["WinHttpQueryDataAvailable","WinHttpQueryDataAvailable function [WinHTTP]","http.winhttpquerydataavailable","winhttp.winhttpquerydataavailable_function","winhttp/WinHttpQueryDataAvailable"]
old-location: http\winhttpquerydataavailable.htm
tech.root: http
ms.assetid: 041ec571-10ed-48d0-9a99-e0b5d9e08f70
ms.date: 12/05/2018
ms.keywords: WinHttpQueryDataAvailable, WinHttpQueryDataAvailable function [WinHTTP], http.winhttpquerydataavailable, winhttp.winhttpquerydataavailable_function, winhttp/WinHttpQueryDataAvailable
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
 - WinHttpQueryDataAvailable
 - winhttp/WinHttpQueryDataAvailable
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
 - WinHttpQueryDataAvailable
---

## -description

The <b>WinHttpQueryDataAvailable</b> function returns the amount of data, in bytes, available to be read with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>.

## -parameters

### -param hRequest [in]

A valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>. <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> must have been called for this handle and have completed before <b>WinHttpQueryDataAvailable</b> is called.

### -param lpdwNumberOfBytesAvailable [out]

A pointer to an unsigned long integer variable that receives the number of available bytes. When WinHTTP is used in asynchronous mode, always set this parameter to <b>NULL</b> and retrieve data in the callback function; not doing so can cause a memory fault.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error data, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_CONNECTION_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered. For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot complete because the handle supplied is not in the correct state.

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
<dt><b>ERROR_WINHTTP_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request has timed out.

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

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function can operate either synchronously or asynchronously.  If it returns <b>FALSE</b>, it failed and you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information. If it returns <b>TRUE</b>, use the WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE completion to determine whether this function was successful and the value of the parameters.  The WINHTTP_CALLBACK_STATUS_REQUEST_ERROR completion indicates that the operation completed asynchronously, but failed.

<div class="alert"><b>Warning</b>  When WinHTTP is used in asynchronous mode, always set the <i>lpdwNumberOfBytesAvailable</i> parameter to <b>NULL</b> and retrieve the bytes available in the callback function; otherwise, a memory fault can occur.</div>
<div> </div>
This function returns the number of bytes of data that are available to read immediately by a subsequent call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>. If no data is available and the end of the file has not been reached, one of two things happens.  If the session is synchronous, the request waits until data becomes available. If the session is asynchronous, the function returns <b>TRUE</b>, and when data becomes available, calls the callback function with WINHTTP_STATUS_CALLBACK_DATA_AVAILABLE and indicates the number of bytes immediately available  to read by calling <b>WinHttpReadData</b>.

The amount of data that remains is not recalculated until all available data indicated by the call to 
<b>WinHttpQueryDataAvailable</b> is read.

Use the return value of <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a> to determine when a response has been completely read. 

<div class="alert"><b>Important</b>  Do not use the return value of <b>WinHttpQueryDataAvailable</b> to determine whether the end of a response has been reached, because not all servers terminate responses properly, and an improperly terminated response causes <b>WinHttpQueryDataAvailable</b> to anticipate more data.</div>
<div> </div>
For 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handles created by the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a> function and sent by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>, a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> must be made on the handle before 
<b>WinHttpQueryDataAvailable</b> can be used.

If a status callback function has been installed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then those of the following notifications  that  have been set in the <i>dwNotificationFlags</i> parameter of <b>WinHttpSetStatusCallback</b> indicate progress in checking for available data:

<ul>
<li>WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE</li>
<li>WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED</li>
<li>WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE</li>
</ul>
<div class="alert"><b>Note</b>  For more information about Windows XP and Windows 2000, see <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.</div>
<div> </div>

## Examples

The following example shows how to use secure transaction semantics to download a resource from an HTTPS server. The sample code initializes the WinHTTP API, selects a target HTTPS server, and then opens and sends a request for this secure resource.  
<b>WinHttpQueryDataAvailable</b> is used with the request handle to determine how much data is available for download, then 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a> is used to read that data.  This process repeats until the entire document has been retrieved and displayed.

> [!IMPORTANT]
> If you want some data as quickly as possible (that is, you're processing and parsing data as you receive it), then you should call **WinHttpQueryDataAvailable** and [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata). If you're trying to download the entire response as quickly as possible, then call **WinHttpReadData** directly, because **WinHttpReadData** tries to fill your buffer before completing.
> 
> Also, the code example below allocates on every loop iteration. For production code, where performance is important, you could instead start with an appropriately-sized buffer (perhaps 1 megabyte), and resize that if necessary. In practice, **WinHttpQueryDataAvailable** returns no more than 8 kilobytes.

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

    // Continue to verify data until there is nothing left.
    if (bResults)
        do 
        {

            // Verify available data.
            dwSize = 0;
            if (!WinHttpQueryDataAvailable( hRequest, &dwSize))
                printf( "Error %u in WinHttpQueryDataAvailable.\n",
                        GetLastError());

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
        printf( "Error %d has occurred.\n", GetLastError());

    // Close open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>