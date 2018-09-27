---
UID: NF:winhttp.WinHttpCloseHandle
title: WinHttpCloseHandle function
author: windows-sdk-content
description: The WinHttpCloseHandle function closes a single HINTERNET handle.
old-location: http\winhttpclosehandle.htm
tech.root: winhttp
ms.assetid: 78215141-dfe8-4f0a-ba1a-a63fa257db6f
ms.author: windowssdkdev
ms.date: 09/11/2018
ms.keywords: WinHttpCloseHandle, WinHttpCloseHandle function [WinHTTP], http.winhttpclosehandle, winhttp.winhttpclosehandle, winhttp/WinHttpCloseHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
---

# WinHttpCloseHandle function


## -description


The <b>WinHttpCloseHandle</b> function closes a single 
<a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle.


## -parameters




### -param hInternet [in]

Valid 
<a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle to be closed. 


## -returns



Returns <b>TRUE</b> if the handle is successfully closed, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Codes</th>
<th>Description</th>
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



Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If there is a status callback registered for the handle being closed and the handle was created with a non-<b>NULL</b> context value, a <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b> callback is made. This  is the last callback made from the handle and indicates that the handle is being destroyed.


An application can terminate an in-progress synchronous or asynchronous request by closing the <a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> request handle using <b>WinHttpCloseHandle</b>. For asynchronous requests, keep the following points in mind:


<ul>
<li>
After an application calls <b>WinHttpCloseHandle</b> on a WinHTTP handle, it cannot call any other WinHTTP API functions using that handle from any thread.

</li>
<li>
Even after a call to <b>WinHttpCloseHandle</b> returns, the application must still be prepared to receive callbacks for the closed handle, because WinHTTP can tear down the handle asynchronously. If the asynchronous request was not able to complete successfully, the callback  receives a WINHTTP_CALLBACK_STATUS_REQUEST_ERROR notification.

</li>
<li>
If an application associates a context data structure or object with the handle, it should maintain that binding until the callback function receives a <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b> notification. This is the last callback notification WinHTTP sends prior to deleting a handle object from memory. In order to receive the <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b> callback notification, the application must enable the <b>WINHTTP_CALLBACK_FLAG_HANDLES</b> flag in the <a href="https://msdn.microsoft.com/b093daf0-7abe-49cb-8c09-9519e3c130b6">WinHttpSetStatusCallback</a> call.

</li>
<li>
Before calling <b>WinHttpCloseHandle</b>, an application can call <a href="https://msdn.microsoft.com/b093daf0-7abe-49cb-8c09-9519e3c130b6">WinHttpSetStatusCallback</a> to indicate that no more callbacks should be made:

<code>WinHttpSetStatusCallback( hRequest, NULL, 0, 0 );</code>

It might seem that the context data structure could then be freed immediately rather than having to wait for a <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b> notification, but this is not the case: WinHTTP does not synchronize <a href="https://msdn.microsoft.com/b093daf0-7abe-49cb-8c09-9519e3c130b6">WinHttpSetStatusCallback</a> with callbacks originating in worker threads. As a result, a callback could already be in progress from another thread, and the application could receive a callback notification even after having <b>NULL</b>ed-out the callback function pointer and deleted the handle's context data structure.  Because of this potential race condition, be conservative in freeing the context structure until after having received the <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b> notification.

</li>
</ul>
An application should never <b>WinHttpCloseHandle</b> call  on a synchronous request. This can create a race condition. See <a href="hinternet_handles_in_winhttp.htm">HINTERNET Handles in WinHTTP</a> for more information.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following example shows you how to  retrieve the connection 
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
            printf("Error %u in WinHttpQueryOption.\n", 
                   GetLastError());
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




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/afcdad8d-687e-4a1f-99d8-5d8be13825fa">WinHttpConnect</a>



<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>



<a href="https://msdn.microsoft.com/9ecd035d-1abf-48ca-baf2-d9754f912c60">WinHttpOpenRequest</a>
 

 

