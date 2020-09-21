---
UID: NF:winhttp.WinHttpResetAutoProxy
title: WinHttpResetAutoProxy function (winhttp.h)
description: Resets the auto-proxy.
helpviewer_keywords: ["WINHTTP_RESET_ALL","WINHTTP_RESET_NOTIFY_NETWORK_CHANGED","WINHTTP_RESET_OUT_OF_PROC","WINHTTP_RESET_SCRIPT_CACHE","WINHTTP_RESET_STATE","WINHTTP_RESET_SWPAD_ALL","WINHTTP_RESET_SWPAD_CURRENT_NETWORK","WinHttpResetAutoProxy","WinHttpResetAutoProxy function [WinHTTP]","http.winhttpresetautoproxy","winhttp/WinHttpResetAutoProxy"]
old-location: http\winhttpresetautoproxy.htm
tech.root: http
ms.assetid: 08b4ea41-4349-4746-a98e-93ba1db20d0e
ms.date: 12/05/2018
ms.keywords: WINHTTP_RESET_ALL, WINHTTP_RESET_NOTIFY_NETWORK_CHANGED, WINHTTP_RESET_OUT_OF_PROC, WINHTTP_RESET_SCRIPT_CACHE, WINHTTP_RESET_STATE, WINHTTP_RESET_SWPAD_ALL, WINHTTP_RESET_SWPAD_CURRENT_NETWORK, WinHttpResetAutoProxy, WinHttpResetAutoProxy function [WinHTTP], http.winhttpresetautoproxy, winhttp/WinHttpResetAutoProxy
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - WinHttpResetAutoProxy
 - winhttp/WinHttpResetAutoProxy
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
 - WinHttpResetAutoProxy
---

# WinHttpResetAutoProxy function


## -description

The <b>WinHttpResetAutoProxy</b> function resets the auto-proxy.

## -parameters

### -param hSession [in]

A valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> WinHTTP session handle returned by a previous call to 
the <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a> function.

### -param dwFlags [in]

A set of flags that affects the reset operation.


The following flags are supported as defined in the <i>Winhttp.h</i> header file.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_STATE"></a><a id="winhttp_reset_state"></a><dl>
<dt><b>WINHTTP_RESET_STATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Forces a flush and retry of non-persistent proxy information on the current network.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_SWPAD_CURRENT_NETWORK"></a><a id="winhttp_reset_swpad_current_network"></a><dl>
<dt><b>WINHTTP_RESET_SWPAD_CURRENT_NETWORK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Flush the PAD information for the current network.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_SWPAD_ALL"></a><a id="winhttp_reset_swpad_all"></a><dl>
<dt><b>WINHTTP_RESET_SWPAD_ALL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Flush the PAD information for all networks.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_SCRIPT_CACHE"></a><a id="winhttp_reset_script_cache"></a><dl>
<dt><b>WINHTTP_RESET_SCRIPT_CACHE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Flush the persistent HTTP cache of proxy scripts.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_ALL"></a><a id="winhttp_reset_all"></a><dl>
<dt><b>WINHTTP_RESET_ALL</b></dt>
<dt>0x0000FFFF</dt>
</dl>
</td>
<td width="60%">
Forces a flush and retry of all proxy information on the current network.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_NOTIFY_NETWORK_CHANGED"></a><a id="winhttp_reset_notify_network_changed"></a><dl>
<dt><b>WINHTTP_RESET_NOTIFY_NETWORK_CHANGED</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Flush the current proxy information and notify that the network changed.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_RESET_OUT_OF_PROC"></a><a id="winhttp_reset_out_of_proc"></a><dl>
<dt><b>WINHTTP_RESET_OUT_OF_PROC</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Act on the autoproxy service instead of the current process.  <div class="alert"><b>Note</b>  This flag is required.</div>
<div> </div>


Applications that use the  <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl">WinHttpGetProxyForUrl</a> function to purge in-process caching should close the <i>hInternet</i> handle and open a new handle for future calls.

</td>
</tr>
</table>

## -returns

A code indicating the success or failure of the operation.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSession</i> parameter is not a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSession</i> parameter is not the product of a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>.

</td>
</tr>
</table>

## -remarks

To reset everything, set the <i>dwFlags</i> parameter to include <b>WINHTTP_RESET_ALL</b> and <b>WINHTTP_RESET_OUT_OF_PROC</b>. 



<div class="alert"><b>Note</b>  If you make subsequent calls to the <b>WinHttpResetAutoProxy</b> function, there must be at least 30 seconds delay between calls to reset the state of the auto-proxy. If there is less than 30 seconds, the <b>WinHttpResetAutoProxy</b> function call may return <b>ERROR_SUCCESS</b> but the reset won't happen. 
</div>
<div> </div>