---
UID: NF:winhttp.WinHttpReadData
title: WinHttpReadData function (winhttp.h)
description: The WinHttpReadData function reads data from a handle opened by the WinHttpOpenRequest function.
helpviewer_keywords: ["WinHttpReadData","WinHttpReadData function [WinHTTP]","http.winhttpreaddata","winhttp.winhttpreaddata_function","winhttp/WinHttpReadData"]
old-location: http\winhttpreaddata.htm
tech.root: http
ms.assetid: 06340601-9b2d-487a-a82a-aa2175a52dc5
ms.date: 12/05/2018
ms.keywords: WinHttpReadData, WinHttpReadData function [WinHTTP], http.winhttpreaddata, winhttp.winhttpreaddata_function, winhttp/WinHttpReadData
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
 - WinHttpReadData
 - winhttp/WinHttpReadData
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
 - WinHttpReadData
---

# WinHttpReadData function


## -description

The <b>WinHttpReadData</b> function reads data from a handle opened by the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a> function.

Also see [WinHttpReadDataEx](nf-winhttp-winhttpreaddataex.md).

## -parameters

### -param hRequest [in]

Valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned from a previous call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>. <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> or <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a> must have been called for this handle and must have completed before <b>WinHttpReadData</b> is called. Although calling <b>WinHttpReadData</b> immediately after completion of <b>WinHttpReceiveResponse</b> avoids the expense of a buffer copy, doing so requires that the application use a fixed-length buffer for reading.

### -param lpBuffer [out]

Pointer to a buffer that receives the data read. Make sure that this buffer remains valid until <b>WinHttpReadData</b> has completed.

### -param dwNumberOfBytesToRead [in]

Unsigned long integer value that contains the number of bytes to read.

### -param lpdwNumberOfBytesRead [out]

Pointer to an unsigned long integer variable that receives the number of bytes read. 
<b>WinHttpReadData</b> sets this value to zero before doing any work or error checking.  When using WinHTTP asynchronously, always set this parameter to <b>NULL</b> and retrieve the information in the callback function; not doing so can cause a memory fault.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table identifies the error codes that are returned.

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
The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered. For example, WinHTTP 5.1 does not support SSL2 unless the client specifically enables it.

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
<dt><b>ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Returned when an incoming response exceeds an internal WinHTTP size limit.

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

Starting in Windows Vista and Windows Server 2008, WinHttp enables applications to perform chunked transfer encoding on data sent to the server. When the Transfer-Encoding header is present on the WinHttp  response, <b>WinHttpReadData</b> strips the chunking information before giving the data to the application.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function can operate either synchronously or asynchronously.  If this function returns <b>FALSE</b>, this function failed and you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information. If this function returns <b>TRUE</b>, use the WINHTTP_CALLBACK_STATUS_READ_COMPLETE completion to determine whether this function was successful and the value of the parameters.  The WINHTTP_CALLBACK_STATUS_REQUEST_ERROR completion indicates that the operation completed asynchronously, but failed.

<div class="alert"><b>Warning</b>  When  WinHTTP is used in asynchronous mode, always set the <i>lpdwNumberOfBytesRead</i> parameter to <b>NULL</b> and retrieve the bytes read in the callback function; otherwise, a memory fault can occur.</div>
<div> </div>
When the read buffer is very small, 
<b>WinHttpReadData</b> might complete synchronously.  If the WINHTTP_CALLBACK_STATUS_READ_COMPLETE completion triggers another call to 
<b>WinHttpReadData</b>, the situation can result in a stack overflow.  In general, it is best to use a read buffer that is comparable in size, or larger than the internal read buffer used by WinHTTP, which is 8 KB.

If you are using <b>WinHttpReadData</b> synchronously, and the return value is <b>TRUE</b> and the number of bytes read is zero, the transfer has been completed and there are no more bytes to read on the handle. This is analogous to reaching end-of-file in a local file. If you are using the function asynchronously, the <a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_CALLBACK_STATUS_READ_COMPLETE</a> callback is called with the <i>dwStatusInformationLength</i> parameter set to zero when the end of a response is found. 

<b>WinHttpReadData</b> tries to fill the buffer pointed to by 
<i>lpBuffer</i> until there is no more data available from the response.  If sufficient data has not arrived from the server, the buffer is not filled.

For 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handles created by the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a> function and sent by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>, a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> must be made on the handle before 
<b>WinHttpReadData</b> can be used.

Single byte characters retrieved with 
<b>WinHttpReadData</b> are not converted to multi-byte characters.

When the read buffer is very small, <b>WinHttpReadData</b> may complete synchronously, and if the <b>WINHTTP_CALLBACK_STATUS_READ_COMPLETE</b> completion then triggers another call to <b>WinHttpReadData</b>, a stack overflow can result. It is best to use a read buffer that is 8 Kilobytes or larger in size.

If sufficient data has not arrived from the server, <b>WinHttpReadData</b> does not entirely fill the buffer pointed to by <i>lpBuffer</i>. The buffer must be large enough at least to hold the HTTP headers on the first read, and when reading HTML encoded directory entries, it must be large enough to hold at least one complete entry.

If a status callback function has been installed by using <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then those of the following notifications  that  have been set in the <i>dwNotificationFlags</i> parameter of <b>WinHttpSetStatusCallback</b> indicate progress in checking for available data:

<ul>
<li>WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE</li>
<li>WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED</li>
<li>WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED</li>
<li>WINHTTP_CALLBACK_STATUS_READ_COMPLETE</li>
</ul>
<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/win32/winhttp/winhttp-start-page#run-time-requirements">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following example shows how to use secure transaction semantics to download a resource from an Secure Hypertext Transfer Protocol (HTTPS) server. The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, then opens and sends a request for this secure resource.  
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a> is used with the request handle to determine how much data is available for download, then 
<b>WinHttpReadData</b> is used to read that data.  This process repeats until the entire document has been retrieved and displayed.


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
    {
        do 
        {
            // Check for available data.
            dwSize = 0;
            if (!WinHttpQueryDataAvailable( hRequest, &dwSize)) 
            {
                printf( "Error %u in WinHttpQueryDataAvailable.\n",
                        GetLastError());
                break;
            }
            
            // No more available data.
            if (!dwSize)
                break;

            // Allocate space for the buffer.
            pszOutBuffer = new char[dwSize+1];
            if (!pszOutBuffer)
            {
                printf("Out of memory\n");
                break;
            }
            
            // Read the Data.
            ZeroMemory(pszOutBuffer, dwSize+1);

            if (!WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                                  dwSize, &dwDownloaded))
            {                                  
                printf( "Error %u in WinHttpReadData.\n", GetLastError());
            }
            else
            {
                printf("%s", pszOutBuffer);
            }
        
            // Free the memory allocated to the buffer.
            delete [] pszOutBuffer;

            // This condition should never be reached since WinHttpQueryDataAvailable
            // reported that there are bits to read.
            if (!dwDownloaded)
                break;
                
        } while (dwSize > 0);
    }
    else
    {
        // Report any errors.
        printf( "Error %d has occurred.\n", GetLastError() );
    }

    // Close any open handles.
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



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwritedata">WinHttpWriteData</a>
