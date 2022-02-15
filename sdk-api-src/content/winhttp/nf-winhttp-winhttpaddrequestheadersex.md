---
UID: NF:winhttp.WinHttpAddRequestHeadersEx
title: WinHttpAddRequestHeadersEx
description: Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.
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
 - WinHttpAddRequestHeadersEx
 - winhttp/WinHttpAddRequestHeadersEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpAddRequestHeadersEx
---

## -description

Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.

## -parameters

### -param hRequest

Type: IN **[HINTERNET](/windows/win32/winhttp/hinternet-handles-in-winhttp)**

An **HINTERNET** handle returned by a call to [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest).

### -param dwModifiers

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

An unsigned long integer value that contains the flags used to modify the semantics of this function. Can be one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_ADD"></a><a id="winhttp_addreq_flag_add"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_ADD</b></dt>
</dl>
</td>
<td width="60%">
Adds the header if it does not exist. Used with 
<b>WINHTTP_ADDREQ_FLAG_REPLACE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_ADD_IF_NEW"></a><a id="winhttp_addreq_flag_add_if_new"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_ADD_IF_NEW</b></dt>
</dl>
</td>
<td width="60%">
Adds the header only if it does not already exist; otherwise, an error is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE"></a><a id="winhttp_addreq_flag_coalesce"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA"></a><a id="winhttp_addreq_flag_coalesce_with_comma"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name using a comma. For example, adding "Accept: text/*" followed by "Accept: audio/*" with this flag results in a single header "Accept: text/*, audio/*". This causes the first header found to be merged. The calling application must  to ensure a cohesive scheme with respect to merged and separate headers.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON"></a><a id="winhttp_addreq_flag_coalesce_with_semicolon"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name using a semicolon.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_REPLACE"></a><a id="winhttp_addreq_flag_replace"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_REPLACE</b></dt>
</dl>
</td>
<td width="60%">
Replaces or removes a header. If the header value is empty and the header is found, it is removed. If the value is not empty, it is replaced.

</td>
</tr>
</table>

### -param ullFlags

Type: IN **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Pass **WINHTTP_EXTENDED_HEADER_FLAG_UNICODE** to indicate that the strings passed in are Unicode strings.

### -param ullExtra

Type: IN **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Reserved.

### -param cHeaders

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of elements in *pHeaders*.

### -param pHeaders

Type: \_In\_reads\_(cHeaders) **[WINHTTP_EXTENDED_HEADER](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)\***

An array of **WINHTTP_EXTENDED_HEADER** structures.

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
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be performed because the handle supplied is not in the correct state.

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
Not enough memory was available to complete the requested operation.

</td>
</tr>
</table>

## -remarks

## -see-also

* [About Microsoft Windows HTTP Services (WinHTTP)](/windows/win32/WinHttp/about-winhttp)
* [WinHTTP versions](/windows/win32/WinHttp/winhttp-versions)
* [WinHttpOpenRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpopenrequest)
* [WinHttpSendRequest](/windows/win32/api/winhttp/nf-winhttp-winhttpsendrequest)
