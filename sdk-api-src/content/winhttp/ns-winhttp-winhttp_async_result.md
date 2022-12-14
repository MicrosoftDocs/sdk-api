---
UID: NS:winhttp._WINHTTP_ASYNC_RESULT
title: WINHTTP_ASYNC_RESULT (winhttp.h)
description: The WINHTTP_ASYNC_RESULT structure contains the result of a call to an asynchronous function. This structure is used with the WINHTTP_STATUS_CALLBACK prototype.
helpviewer_keywords: ["*LPWINHTTP_ASYNC_RESULT","API_QUERY_DATA_AVAILABLE","API_READ_DATA","API_RECEIVE_RESPONSE","API_SEND_REQUEST","API_WRITE_DATA","WINHTTP_ASYNC_RESULT","WINHTTP_ASYNC_RESULT structure [HTTP]","http.winhttp_async_result","winhttp.winhttp_async_result_structure","winhttp/WINHTTP_ASYNC_RESULT"]
old-location: http\winhttp_async_result.htm
tech.root: http
ms.assetid: 31544ef1-2532-4e44-8747-7a693cef9ccd
ms.date: 12/05/2018
ms.keywords: '*LPWINHTTP_ASYNC_RESULT, API_QUERY_DATA_AVAILABLE, API_READ_DATA, API_RECEIVE_RESPONSE, API_SEND_REQUEST, API_WRITE_DATA, WINHTTP_ASYNC_RESULT, WINHTTP_ASYNC_RESULT structure [HTTP], http.winhttp_async_result, winhttp.winhttp_async_result_structure, winhttp/WINHTTP_ASYNC_RESULT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINHTTP_ASYNC_RESULT, *LPWINHTTP_ASYNC_RESULT
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - LPWINHTTP_ASYNC_RESULT
 - winhttp/LPWINHTTP_ASYNC_RESULT
 - WINHTTP_ASYNC_RESULT
 - winhttp/WINHTTP_ASYNC_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_ASYNC_RESULT
---

## -description

The <b>WINHTTP_ASYNC_RESULT</b> structure contains the result of a call to an asynchronous function. This structure is used with the 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> prototype.

## -struct-fields

### -field dwResult

Return value from an asynchronous Microsoft Windows HTTP Services (WinHTTP) function. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="API_RECEIVE_RESPONSE"></a><a id="api_receive_response"></a><dl>
<dt><b>API_RECEIVE_RESPONSE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="API_QUERY_DATA_AVAILABLE"></a><a id="api_query_data_available"></a><dl>
<dt><b>API_QUERY_DATA_AVAILABLE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="API_READ_DATA"></a><a id="api_read_data"></a><dl>
<dt><b>API_READ_DATA</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="API_WRITE_DATA"></a><a id="api_write_data"></a><dl>
<dt><b>API_WRITE_DATA</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwritedata">WinHttpWriteData</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="API_SEND_REQUEST"></a><a id="api_send_request"></a><dl>
<dt><b>API_SEND_REQUEST</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>.
</td>
</tr>

<tr>
<td width="40%"><a id="API_GET_PROXY_FOR_URL"></a><a id="api_get_proxy_for_url"></a><dl>
<dt><b>API_GET_PROXY_FOR_URL</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The error occurred during a call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a>.
</td>
</tr>
</table>

### -field dwError

Contains the error code if 
<b>dwResult</b> indicates that the function failed.

## -remarks

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP
		  Versions</a>
