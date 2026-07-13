---
UID: NF:winhttp.WinHttpQueryHeadersEx
title: WinHttpQueryHeadersEx
description: Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.
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
 - WinHttpQueryHeadersEx
 - winhttp/WinHttpQueryHeadersEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpQueryHeadersEx
---

## -description

Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.

## -parameters

### -param hRequest

Type: \_In\_ **[HINTERNET](/windows/win32/winhttp/hinternet-handles-in-winhttp)**

Request handle returned by [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest). The [WinHttpReceiveResponse](/windows/win32/api/winhttp/nf-winhttp-winhttpreceiveresponse) call for this handle must have completed before calling **WinHttpQueryHeadersEx**. If you're querying trailers, then the [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata) call for this handle must return 0 bytes read before calling **WinHttpQueryHeadersEx**.

### -param dwInfoLevel

Type: \_In\_ **[DWORD](/windows/win32/winprog/windows-data-types)**

Value of type <b>DWORD</b> that specifies a combination of attribute and modifier flags listed in the 
<a href="/windows/desktop/WinHttp/query-info-flags">Query info flags</a> topic. These attribute and modifier flags indicate the information that is being requested, and how it is to be formatted.

> [!NOTE]
> The following flags return **ERROR_INVALID_PARAMETER** if used: **WINHTTP_QUERY_VERSION**, **WINHTTP_QUERY_STATUS_CODE**, **WINHTTP_QUERY_STATUS_TEXT**, **WINHTTP_QUERY_FLAG_NUMBER**, **WINHTTP_QUERY_FLAG_NUMBER64**, **WINHTTP_QUERY_FLAG_SYSTEMTIME**, and **WINHTTP_QUERY_RAW_HEADERS_CRLF**.

The flag **WINHTTP_QUERY_EX_ALL_HEADERS** returns all the headers.

If you're not querying for all of the headers, then you can pass the flag corresponding to a specific known header, or you can pass **WINHTTP_QUERY_CUSTOM** along with a string for the header name in the *pHeaderName* parameter.

Passing **WINHTTP_QUERY_FLAG_WIRE_ENCODING** returns the headers in the format in which they're sent over the wire (you should access/set the *psz\** members of [WINHTTP_EXTENDED_HEADER](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header) and [WINHTTP_HEADER_NAME](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)). If you don't set the wire encoding flag, then the default behavior is to return headers in Unicode format (you should access/set the *pwsz\** members of [WINHTTP_EXTENDED_HEADER](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header) and [WINHTTP_HEADER_NAME](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)).

### -param ullFlags

Type: \_In\_ **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Reserved. Set to 0.

### -param uiCodePage

Type: \_In\_ **[UINT](/windows/win32/winprog/windows-data-types)**

The code page to use for Unicode conversion. You should pass in 0 for default behavior (CP_ACP), or when using **WINHTTP_QUERY_FLAG_WIRE_ENCODING**. No validation is done for this parameter.

### -param pdwIndex

Type: \_Inout\_opt\_ **[PDWORD](/windows/win32/winprog/windows-data-types)**

The address of a zero-based index used to enumerate multiple headers with the same name. When calling the function, this parameter is the index of the specified header to return. When the function returns, this parameter is the index of the next header. Pass **NULL** to access the first instance of a given header.

### -param pHeaderName

Type: \_Inout\_opt\_ **[PWINHTTP_HEADER_NAME](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)**

The address of a [WINHTTP_HEADER_NAME](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name) structure.

Set *pHeaderName* to **NULL** when retrieving all headers. If this parameter is not **NULL**, and you pass **WINHTTP_QUERY_CUSTOM** with *dwInfoLevel*, then **WinHttpQueryHeadersEx** will retrieve only the header specified by this parameter. If you pass **WINHTTP_QUERY_FLAG_WIRE_ENCODING** with *dwInfoLevel*, then you should use the *pszName* member (if the flag is not set, then use *pwszName* member).

### -param pBuffer

Type: \_Out\_writes\_bytes\_to\_opt\_(*pdwBufferLength, *pdwBufferLength) **[LPVOID](/windows/win32/winprog/windows-data-types)**

A caller-provided buffer to store the parsed header pointers and the headers. If this parameter is **NULL** or too small, then **WinHttpQueryHeadersEx** returns **ERROR_INSUFFICIENT_BUFFER**, and the *pdwBufferLength* parameter contains the required buffer size in bytes.

### -param pdwBufferLength

Type: \_Inout\_ **[PDWORD](/windows/win32/winprog/windows-data-types)**

Length of the caller-provided buffer. If *pBuffer* is **NULL** or too small, then **WinHttpQueryHeadersEx** writes the required buffer size in bytes to this parameter.

### -param ppHeaders

Type: \_Out\_writes\_opt\_(*pdwHeadersCount) **[PWINHTTP_EXTENDED_HEADER](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)\***

A handle to an array of [WINHTTP_EXTENDED_HEADER](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header) for accessing parsed header names/values. You should pass in the address of a **WINHTTP_EXTENDED_HEADER** pointer that's initialized to **NULL**. Upon completion, you should access the *pszName*/*pszValue* parameters if using **WINHTTP_QUERY_FLAG_WIRE_ENCODING**, and *pwszName*/*pwszValue* otherwise.

### -param pdwHeadersCount

Type: \_Out\_ **[PDWORD](/windows/win32/winprog/windows-data-types)**

The number of headers returned. You shouldn't try to access beyond `ppHeaders[cHeaders - 1]`, because that is out of bounds of the array.

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

**WinHttpQueryHeadersEx** builds on the functionality of [WinHttpQueryHeaders](nf-winhttp-winhttpqueryheaders.md). **WinHttpQueryHeaders** allows you to query request or response headers (or response trailers) in the form of a string, a number (DWORD), or a timestamp (SYSTEMTIME). Querying for all headers returns a single serialized string with CRLF or NULL characters delimiting different headers. For example, "Name1: value1\r\nName2: value2\r\n\r\n". Or "Name1: value1\0Name2: value2\0\0". A double delimiter is used to indicate the end of the string.

**WinHttpQueryHeadersEx** gives you a way to retrieve parsed header name and value strings.

## -see-also
