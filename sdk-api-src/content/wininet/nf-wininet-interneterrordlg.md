---
UID: NF:wininet.InternetErrorDlg
title: InternetErrorDlg function (wininet.h)
description: Displays a dialog box for the error that is passed to InternetErrorDlg, if an appropriate dialog box exists.
helpviewer_keywords: ["InternetErrorDlg","InternetErrorDlg function [WinINet]","_inet_interneterrordlg_function","wininet.interneterrordlg","wininet/InternetErrorDlg"]
old-location: wininet\interneterrordlg.htm
tech.root: wininet
ms.assetid: 09384ba9-e5cc-48fd-a52c-15df223f87dc
ms.date: 12/05/2018
ms.keywords: InternetErrorDlg, InternetErrorDlg function [WinINet], _inet_interneterrordlg_function, wininet.interneterrordlg, wininet/InternetErrorDlg
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetErrorDlg
 - wininet/InternetErrorDlg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetErrorDlg
---

# InternetErrorDlg function


## -description

Displays a dialog box for the error that is passed to 
<b>InternetErrorDlg</b>, if an appropriate dialog box exists. If the 
<b>FLAGS_ERROR_UI_FILTER_FOR_ERRORS</b> flag is used, the function also checks the headers for any hidden errors and displays a dialog box if needed.

## -parameters

### -param hWnd [in]

Handle to the parent window for any needed dialog box. If no dialog box is needed and <b>FLAGS_ERROR_UI_FLAGS_NO_UI</b> is passed to <i>dwFlags</i>, then this parameter can be <b>NULL</b>.

### -param hRequest [in, out]

Handle to the Internet connection used in the call to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a>.

### -param dwError [in]

Error value for which to display a dialog box. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION</dt>
</dl>
</td>
<td width="60%">
Allows the user to confirm the redirect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT</dt>
</dl>
</td>
<td width="60%">
Displays a dialog indicating that the auto proxy script is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_CHG_POST_IS_NON_SECURE</dt>
</dl>
</td>
<td width="60%">
Displays a dialog asking the user whether to post the given data on a non-secure channel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED</dt>
</dl>
</td>
<td width="60%">
The server is requesting a client certificate.

The return value for this error is always  ERROR_SUCCESS, regardless of whether or not the user has selected a certificate. If the user has not selected a certificate then anonymous client authentication will be attempted on the subsequent request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR</dt>
</dl>
</td>
<td width="60%">
Notifies the user of the zone crossing to a secure site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR</dt>
</dl>
</td>
<td width="60%">
Notifies the user of the zone crossing from a secure site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR</dt>
</dl>
</td>
<td width="60%">
Notifies the user that the data being posted is now being redirected to a non-secure site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_INCORRECT_PASSWORD</dt>
</dl>
</td>
<td width="60%">
Displays a dialog box requesting the user's name and password.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_INVALID_CA</dt>
</dl>
</td>
<td width="60%">
Indicates that the SSL certificate Common Name (host name field) is incorrect. Displays an Invalid SSL Common Name dialog box and lets the user view the incorrect certificate. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_MIXED_SECURITY</dt>
</dl>
</td>
<td width="60%">
Displays a warning to the user concerning mixed secure and non-secure content.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_POST_IS_NON_SECURE</dt>
</dl>
</td>
<td width="60%">
Displays a dialog asking the user whether to post the given data on a non-secure channel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_SEC_CERT_CN_INVALID</dt>
</dl>
</td>
<td width="60%">
Indicates that the SSL certificate Common Name (host name field) is incorrect. Displays an Invalid SSL Common Name dialog box and lets the user view the incorrect certificate. Also allows the user to select a certificate in response to a server request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_SEC_CERT_ERRORS</dt>
</dl>
</td>
<td width="60%">
Displays a warning to the user showing the issues with the server certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_SEC_CERT_DATE_INVALID</dt>
</dl>
</td>
<td width="60%">
Tells the user that the SSL certificate has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_SEC_CERT_REV_FAILED</dt>
</dl>
</td>
<td width="60%">
Displays a warning to the user showing that the server certificate’s revocation check failed.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_SEC_CERT_REVOKED</dt>
</dl>
</td>
<td width="60%">
Displays a dialog indicating that the server certificate is revoked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT</dt>
</dl>
</td>
<td width="60%">
Displays a dialog indicating that the auto proxy script could not be downloaded.

</td>
</tr>
</table>

### -param dwFlags [in]

Actions. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FLAGS_ERROR_UI_FILTER_FOR_ERRORS</dt>
</dl>
</td>
<td width="60%">
Scans the returned headers for errors. Call <b>InternetErrorDlg</b> with this flag set following a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> so as to detect hidden errors. Authentication errors, for example, are normally hidden because the call to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> completes successfully, but by scanning the status codes,  <b>InternetErrorDlg</b> can determine that the proxy or server requires authentication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS</dt>
</dl>
</td>
<td width="60%">
If the function succeeds, stores the results of the dialog box in the Internet handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FLAGS_ERROR_UI_FLAGS_GENERATE_DATA</dt>
</dl>
</td>
<td width="60%">
Queries the Internet handle for needed information. The function constructs the appropriate data structure for the error. (For example, for Cert CN failures, the function grabs the certificate.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FLAGS_ERROR_UI_SERIALIZE_DIALOGS</dt>
</dl>
</td>
<td width="60%">
Serializes authentication dialog boxes for concurrent requests on a password cache entry. The 
<i>lppvData</i> parameter should contain the address of a pointer to an 
<a href="/windows/win32/api/wininet/ns-wininet-internet_per_conn_optionw">INTERNET_AUTH_NOTIFY_DATA</a> structure, and the client should implement a thread-safe, non-blocking callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FLAGS_ERROR_UI_FLAGS_NO_UI</dt>
</dl>
</td>
<td width="60%">
Allows the caller to pass <b>NULL</b> to the <i>hWnd</i> parameter without error.  To be used in circumstances in which no user interface is required.

</td>
</tr>
</table>

### -param lppvData [in, out]

Pointer  to the address of a data structure. The structure can be different for each error that needs to be handled.

## -returns

Returns one of the following values, or an error value otherwise.

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
The function completed successfully.

For more information, see <b>ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED</b> in the <i>dwError</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The function was canceled by the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERNET_FORCE_RETRY</b></dt>
</dl>
</td>
<td width="60%">
This indicates that the function needs to redo its request.  In the case of authentication this indicates that the user clicked the <b>OK</b> button.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle to the parent window is invalid.

</td>
</tr>
</table>

## -remarks

Always inform the user  when any of the following events occur:<ul>
<li>ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR</li>
<li>ERROR_INTERNET_INVALID_CA</li>
<li>ERROR_INTERNET_POST_IS_NON_SECURE</li>
<li>ERROR_INTERNET_SEC_CERT_CN_INVALID</li>
<li>ERROR_INTERNET_SEC_CERT_DATE_INVALID</li>
</ul>Unless the user has explicitly chosen not to be informed of these events, failure to do so exposes the user involuntarily to  a significant security risk.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>