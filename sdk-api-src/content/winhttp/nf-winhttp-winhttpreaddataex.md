---
UID: NF:winhttp.WinHttpReadDataEx
title: WinHttpReadDataEx
description: Reads data from a handle opened by the [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest) function.
tech.root: http
ms.date: 06/30/2021
req.construct-type: function
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.redist: 
f1_keywords:
 - WinHttpReadDataEx
 - winhttp/WinHttpReadDataEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpReadDataEx
---

## -description

Reads data from a handle opened by the [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest) function.

## -parameters

### -param hRequest

Type: IN **[HINTERNET](/windows/win32/winhttp/hinternet-handles-in-winhttp)**

An **HINTERNET** handle returned from a previous call to [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest).

<a href="/windows/win32/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> or <a href="/windows/win32/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a> must have been called for this handle and must have completed before <b>WinHttpReadDataEx</b> is called. Although calling <b>WinHttpReadDataEx</b> immediately after completion of <b>WinHttpReceiveResponse</b> avoids the expense of a buffer copy, doing so requires that your application use a fixed-length buffer for reading.

### -param lpBuffer

Type: \_Out\_writes\_bytes\_to\_(dwNumberOfBytesToRead, *lpdwNumberOfBytesRead) \_\_out\_data\_source(NETWORK) **[LPVOID](/windows/win32/winprog/windows-data-types)**

Pointer to a buffer that receives the data read. Make sure that this buffer remains valid until <b>WinHttpReadDataEx</b> has completed.

### -param dwNumberOfBytesToRead

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

Unsigned long integer value that contains the number of bytes to read.

### -param lpdwNumberOfBytesRead

Type: OUT **[LPDWORD](/windows/win32/winprog/windows-data-types)**

Pointer to an unsigned long integer variable that receives the number of bytes read. 
<b>WinHttpReadDataEx</b> sets this value to zero before doing any work or error checking. When using WinHTTP asynchronously, always set this parameter to <b>NULL</b> and retrieve the information in the callback function; not doing so can cause a memory fault.

### -param ullFlags

Type: IN **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

If you pass **WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**, then WinHttp won't complete the call to **WinHttpReadDataEx** until the provided data buffer has been filled, or the response is complete. Passing this flag makes the behavior of this API equivalent to that of [WinHttpReadData](nf-winhttp-winhttpreaddata.md).

### -param cbProperty

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

Reserved. Pass 0.

### -param pvProperty

Type: \_In\_reads\_bytes\_opt\_(cbProperty) **[PVOID](/windows/win32/winprog/windows-data-types)**

Reserved. Pass NULL.

## -returns

A status code indicating the result of the operation. Among the error codes returned are the following.

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

By default, **WinHttpReadDataEx** returns after any amount of data has been written to the buffer that you provide (the function won't always completely fill the buffer that you provide).

## -see-also

* [About Microsoft Windows HTTP Services (WinHTTP)](/windows/win32/WinHttp/about-winhttp)
* [WinHTTP versions](/windows/win32/WinHttp/winhttp-versions)
* [WinHttpCloseHandle](/windows/win32/api/winhttp/nf-winhttp-winhttpclosehandle)
* [WinHttpConnect](/windows/win32/api/winhttp/nf-winhttp-winhttpconnect)
* [WinHttpOpen](/windows/win32/api/winhttp/nf-winhttp-winhttpopen)
* [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest)
* [WinHttpQueryDataAvailable](/windows/win32/api/winhttp/nf-winhttp-winhttpquerydataavailable)
* [WinHttpReadDataEx](nf-winhttp-winhttpreaddataex.md)
* [WinHttpSendRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpsendrequest)
* [WinHttpWriteData](/windows/win32/api/winhttp/nf-winhttp-winhttpwritedata)
