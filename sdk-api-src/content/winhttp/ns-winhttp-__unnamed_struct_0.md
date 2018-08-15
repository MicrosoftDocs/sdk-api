---
UID: NS:winhttp.__unnamed_struct_0
title: WINHTTP_ASYNC_RESULT
author: windows-sdk-content
description: The WINHTTP_ASYNC_RESULT structure contains the result of a call to an asynchronous function. This structure is used with the WINHTTP_STATUS_CALLBACK prototype.
old-location: http\winhttp_async_result.htm
old-project: winhttp
ms.assetid: 31544ef1-2532-4e44-8747-7a693cef9ccd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWINHTTP_ASYNC_RESULT, API_QUERY_DATA_AVAILABLE, API_READ_DATA, API_RECEIVE_RESPONSE, API_SEND_REQUEST, API_WRITE_DATA, WINHTTP_ASYNC_RESULT, WINHTTP_ASYNC_RESULT structure [HTTP], http.winhttp_async_result, winhttp.winhttp_async_result_structure, winhttp/WINHTTP_ASYNC_RESULT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winhttp.h
req.include-header: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
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
tech.root: 
req.typenames: WINHTTP_ASYNC_RESULT, *LPWINHTTP_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_ASYNC_RESULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WINHTTP_ASYNC_RESULT structure


## -description


The <b>WINHTTP_ASYNC_RESULT</b> structure contains the result of a call to an asynchronous function. This structure is used with the 
<a href="https://msdn.microsoft.com/4d828e41-9073-407a-aab5-531f1d6d6d02">WINHTTP_STATUS_CALLBACK</a> prototype.


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
<a href="https://msdn.microsoft.com/0b79e73b-9f6a-42eb-9108-1ba142ad7c48">WinHttpReceiveResponse</a>.

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
<a href="https://msdn.microsoft.com/041ec571-10ed-48d0-9a99-e0b5d9e08f70">WinHttpQueryDataAvailable</a>.

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
<a href="https://msdn.microsoft.com/06340601-9b2d-487a-a82a-aa2175a52dc5">WinHttpReadData</a>.

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
<a href="https://msdn.microsoft.com/c8b94285-1b01-451b-9803-cc1bacb015ff">WinHttpWriteData</a>.

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
<a href="https://msdn.microsoft.com/991bf531-2e6b-4581-8069-f75789915522">WinHttpSendRequest</a>.

</td>
</tr>
</table>
 


### -field dwError

Contains the error code if 
<b>dwResult</b> indicates that the function failed.


## -remarks



<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

