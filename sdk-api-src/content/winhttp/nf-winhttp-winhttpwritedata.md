---
UID: NF:winhttp.WinHttpWriteData
title: WinHttpWriteData function (winhttp.h)
description: The WinHttpWriteData function writes request data to an HTTP server.
helpviewer_keywords: ["WinHttpWriteData","WinHttpWriteData function [WinHTTP]","http.winhttpwritedata","winhttp.winhttpwritedata_function","winhttp/WinHttpWriteData"]
old-location: http\winhttpwritedata.htm
tech.root: http
ms.assetid: c8b94285-1b01-451b-9803-cc1bacb015ff
ms.date: 12/05/2018
ms.keywords: WinHttpWriteData, WinHttpWriteData function [WinHTTP], http.winhttpwritedata, winhttp.winhttpwritedata_function, winhttp/WinHttpWriteData
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
 - WinHttpWriteData
 - winhttp/WinHttpWriteData
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
 - WinHttpWriteData
---

# WinHttpWriteData function


## -description

The <b>WinHttpWriteData</b> function writes request data to an HTTP server.

## -parameters

### -param hRequest [in]

Valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>. Wait until <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> has completed before calling  this function.

### -param lpBuffer [in]

Pointer to a buffer that contains the data to be sent to the server. Be sure that this buffer remains valid until after <b>WinHttpWriteData</b> completes.

### -param dwNumberOfBytesToWrite [in]

Unsigned long integer value that contains the number of bytes to be written to the file.

### -param lpdwNumberOfBytesWritten [out]

Pointer to an unsigned long integer variable that receives the number of bytes written to the buffer. The 
<b>WinHttpWriteData</b> function sets this value to zero before doing any work or error checking.  When using WinHTTP asynchronously, this parameter must be set to <b>NULL</b> and retrieve the information in the callback function. Not doing so can cause a memory fault.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are:

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

Even when  WinHTTP is  used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function can operate either synchronously or asynchronously.  If this function returns <b>FALSE</b>, you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information. If this function returns <b>TRUE</b>, use the WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE completion to determine whether this function was successful and the value of the parameters.  The WINHTTP_CALLBACK_STATUS_REQUEST_ERROR completion indicates that the operation completed asynchronously, but failed.

<div class="alert"><b>Warning</b>  When using WinHTTP asynchronously, always set the <i>lpdwNumberOfBytesWritten</i> parameter to <b>NULL</b> and retrieve the bytes written in the callback function; otherwise, a memory fault can occur.</div>
<div> </div>
When the application is sending data, it can call 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> to end the data transfer.  If 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> is called, then the data transfer is aborted.

If a status callback function has been installed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then those of the following notifications  that  have been set in the <i>dwNotificationFlags</i> parameter of <b>WinHttpSetStatusCallback</b> indicate progress in sending data to the server:

<ul>
<li>WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE</li>
<li>WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED</li>
<li>WINHTTP_CALLBACK_STATUS_DATA_WRITTEN </li>
<li>WINHTTP_CALLBACK_STATUS_SENDING_REQUEST</li>
<li>WINHTTP_CALLBACK_STATUS_REQUEST_SENT</li>
<li>WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE</li>
</ul>
Two issues can arise when attempting to POST (or PUT) data to proxies or servers that challenge using NTLM or Negotiate authentication. 
 
First, these proxies or servers may send 401/407 challenges and close the connection before all the data can be POST'ed, in which case not only does <b>WinHttpWriteData</b> fail, but also WinHTTP cannot handle the authentication challenges. NTLM and Negotiate require that all authentication handshakes be exchanged on the same socket connection, so authentication fails if the connection is broken prematurely.

Secondly, NTLM and Negotiate may require multiple handshakes to complete authentication, which requires data to be re-POST'ed for each authentication legs. This  can be very inefficient for large data uploads.

To work around these two issues, one solution is to send an idempotent warm-up request such as HEAD to the authenticating v-dir first, handle the authentication challenges associated with this request, and only then POST data. As long as the same socket is re-used to handle the POST'ing,  no further authentication challenges should be encountered and all data can be uploaded at once. Since an authenticated socket can only be reused for subsequent requests within the same session, the POST should  go out in the same socket as long as the socket is not pooled with concurrent requests  competing for it.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHTTP start page.</div>
<div> </div>

#### Examples

This example shows code that  writes data to an HTTP server.  The server name supplied in the example, www.wingtiptoys.com, is fictitious and must be replaced with the name of a server for which you have write access.


```cpp
    PCSTR pszData = "WinHttpWriteData Example";
    DWORD dwBytesWritten = 0;
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
        hConnect = WinHttpConnect( hSession, L"www.wingtiptoys.com",
                                   INTERNET_DEFAULT_HTTP_PORT, 0);

    // Create an HTTP Request handle.
    if (hConnect)
        hRequest = WinHttpOpenRequest( hConnect, L"PUT", 
                                       L"/writetst.txt", 
                                       NULL, WINHTTP_NO_REFERER, 
                                       WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                       0);

    // Send a Request.
    if (hRequest) 
        bResults = WinHttpSendRequest( hRequest, 
                                       WINHTTP_NO_ADDITIONAL_HEADERS,
                                       0, WINHTTP_NO_REQUEST_DATA, 0, 
                                       (DWORD)strlen(pszData), 0);

    // Write data to the server.
    if (bResults)
        bResults = WinHttpWriteData( hRequest, pszData, 
                                     (DWORD)strlen(pszData), 
                                     &dwBytesWritten);

    // End the request.
    if (bResults)
        bResults = WinHttpReceiveResponse( hRequest, NULL);

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



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>