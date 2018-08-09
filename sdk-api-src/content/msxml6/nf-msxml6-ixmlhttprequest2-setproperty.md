---
UID: NF:msxml6.IXMLHTTPRequest2.SetProperty
title: IXMLHTTPRequest2::SetProperty
author: windows-sdk-content
description: Sets a property on an outgoing HTTP request.
old-location: ixhr2\ixmlhttprequest2_setproperty.htm
old-project: ixhr2
ms.assetid: 4BBA4E21-29ED-413D-90D6-161D31CC13C9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],SetProperty method, IXMLHTTPRequest2.SetProperty, IXMLHTTPRequest2::SetProperty, SetProperty, SetProperty method [XMLHttpRequest2], SetProperty method [XMLHttpRequest2],IXMLHTTPRequest2 interface, XHR_PROP_EXTENDED_ERROR, XHR_PROP_IGNORE_CERT_ERRORS, XHR_PROP_NO_AUTH, XHR_PROP_NO_CACHE, XHR_PROP_NO_CRED_PROMPT, XHR_PROP_NO_DEFAULT_HEADERS, XHR_PROP_QUERY_STRING_UTF8, XHR_PROP_REPORT_REDIRECT_STATUS, XHR_PROP_TIMEOUT, ixhr2.ixmlhttprequest2_setproperty, msxml6/IXMLHTTPRequest2::SetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XHR_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.SetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest2::SetProperty


## -description


Sets a property on an outgoing HTTP request.


## -parameters




### -param eProperty [in]

The following values are valid:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_CRED_PROMPT"></a><a id="xhr_prop_no_cred_prompt"></a><dl>
<dt><b>XHR_PROP_NO_CRED_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
Suppresses automatic prompts for user credentials

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_AUTH"></a><a id="xhr_prop_no_auth"></a><dl>
<dt><b>XHR_PROP_NO_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Suppresses authentication that the HTTP stack performs on behalf of the application

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_TIMEOUT"></a><a id="xhr_prop_timeout"></a><dl>
<dt><b>XHR_PROP_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Sets all timeout values to the value given by <i>ullValue</i>, in milliseconds.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_DEFAULT_HEADERS"></a><a id="xhr_prop_no_default_headers"></a><dl>
<dt><b>XHR_PROP_NO_DEFAULT_HEADERS</b></dt>
</dl>
</td>
<td width="60%">
Suppresses adding default headers to the HTTP request.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_REPORT_REDIRECT_STATUS"></a><a id="xhr_prop_report_redirect_status"></a><dl>
<dt><b>XHR_PROP_REPORT_REDIRECT_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Causes the HTTP stack to call the <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> method with an interim redirecting status code.  The <b>OnHeadersAvailable</b> method will be called again for additional redirects and the final destination status code.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_CACHE"></a><a id="xhr_prop_no_cache"></a><dl>
<dt><b>XHR_PROP_NO_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Suppresses cache reads and writes for the HTTP request.

This property is supported by the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_EXTENDED_ERROR"></a><a id="xhr_prop_extended_error"></a><dl>
<dt><b>XHR_PROP_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Causes the HTTP stack to provide HRESULTS with the underlying Win32 error code to the <a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a> method in case of failure.

This property is supported by the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_QUERY_STRING_UTF8_"></a><a id="xhr_prop_query_string_utf8_"></a><dl>
<dt><b>XHR_PROP_QUERY_STRING_UTF8 </b></dt>
</dl>
</td>
<td width="60%">
Causes the query string to be encoded in UTF-8 instead of ACP for the HTTP request.

This property is supported by the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_IGNORE_CERT_ERRORS"></a><a id="xhr_prop_ignore_cert_errors"></a><dl>
<dt><b>XHR_PROP_IGNORE_CERT_ERRORS</b></dt>
</dl>
</td>
<td width="60%">
Suppresses certain certificate errors.

This property is supported by the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface.

</td>
</tr>
</table>
 


### -param ullValue [in]

Specifies the number of milliseconds that the application waits before timing out.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_CRED_PROMPT"></a><a id="xhr_prop_no_cred_prompt"></a><dl>
<dt><b>XHR_PROP_NO_CRED_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
This parameter can be one of the values from the <a href="https://msdn.microsoft.com/01160bda-0d4c-46fc-92ba-82fe5808e665">XHR_CRED_PROMPT</a> enumeration type defined in the <i>Msxml6.h</i>  header file.

<ul>
<li><b>XHR_CRED_PROMPT_ALL</b> if credential prompting should be enabled <b>(default)</b>.</li>
<li><b>XHR_CRED_PROMPT_NONE</b> if credential prompting should be disabled.</li>
<li><b>XHR_CRED_PROMPT_PROXY</b> if credential prompting should only be enabled for proxy authentication.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_AUTH"></a><a id="xhr_prop_no_auth"></a><dl>
<dt><b>XHR_PROP_NO_AUTH</b></dt>
</dl>
</td>
<td width="60%">
This parameter can be one of the values from the <a href="https://msdn.microsoft.com/01160bda-0d4c-46fc-92ba-82fe5808e665">XHR_AUTH</a> enumeration type defined in the <i>Msxml6.h</i>  header file.

<ul>
<li><b>XHR_AUTH_ALL</b> if authentication is enabled <b>(default)</b>.
</li>
<li><b>XHR_AUTH_NONE</b> if authentication is disabled.
</li>
<li><b>XHR_AUTH_PROXY</b> if authentication should only be enabled for proxy authentication.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_TIMEOUT_"></a><a id="xhr_prop_timeout_"></a><dl>
<dt><b>XHR_PROP_TIMEOUT </b></dt>
</dl>
</td>
<td width="60%">
The number of milliseconds, up to 0xFFFFFFFF, that the app waits before timing out.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_DEFAULT_HEADERS"></a><a id="xhr_prop_no_default_headers"></a><dl>
<dt><b>XHR_PROP_NO_DEFAULT_HEADERS</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to enable adding default headers <b>(default)</b>. 
</li>
<li>TRUE(0x1) to disable adding default headers. 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_REPORT_REDIRECT_STATUS"></a><a id="xhr_prop_report_redirect_status"></a><dl>
<dt><b>XHR_PROP_REPORT_REDIRECT_STATUS</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to not report redirect status <b>(default)</b>. 
</li>
<li>TRUE(0x1) to report redirect status. 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_NO_CACHE"></a><a id="xhr_prop_no_cache"></a><dl>
<dt><b>XHR_PROP_NO_CACHE</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to enable caching <b>(default)</b>. 
</li>
<li>TRUE(0x1) to disable caching. 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_EXTENDED_ERROR"></a><a id="xhr_prop_extended_error"></a><dl>
<dt><b>XHR_PROP_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to not provide extended errors <b>(default)</b>. 
</li>
<li>TRUE(0x1) to provide extended errors . 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_QUERY_STRING_UTF8"></a><a id="xhr_prop_query_string_utf8"></a><dl>
<dt><b>XHR_PROP_QUERY_STRING_UTF8</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to not encode the query string in UTF-8 <b>(default)</b>. 
</li>
<li>TRUE(0x1) to encode the query string in UTF-8. 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XHR_PROP_IGNORE_CERT_ERRORS_"></a><a id="xhr_prop_ignore_cert_errors_"></a><dl>
<dt><b>XHR_PROP_IGNORE_CERT_ERRORS </b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>FALSE(0x0) to not ignore certificate errors <b>(default)</b>. 
</li>
<li>TRUE(0x1) to ignore certificate errors. 
</li>
</ul>
</td>
</tr>
</table>
 


## -returns



Returns <b>S_OK</b> on success.




## -remarks



The <b>SetProperty</b> method on the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface is extended on the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface with new properties to support new scenarios:


<ul>
<li>XHR_PROP_NO_CACHE – Suppresses cache reads and writes for the HTTP request.</li>
<li>XHR_PROP_EXTENDED_ERROR – Causes the HTTP stack to provide HRESULTS with the underlying Win32 error code to the OnError method in case of failure.</li>
<li>XHR_PROP_QUERY_STRING_UTF8 – Causes the query string to be encoded in UTF-8 instead of ACP for HTTP request.</li>
<li>XHR_PROP_IGNORE_CERT_ERRORS – Suppresses certain server certificate errors.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<a href="https://msdn.microsoft.com/FE317413-F1A2-4FD7-9DB1-67410C912AF2">XHR_PROPERTY Enumeration</a>
 

 

