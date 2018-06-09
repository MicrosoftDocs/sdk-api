---
UID: NN:wuapi.IWebProxy
title: IWebProxy
author: windows-sdk-content
description: Contains the HTTP proxy settings.
old-location: wua\iwebproxy.htm
old-project: Wua_Sdk
ms.assetid: acc09635-7370-475f-9c3a-a5faaa8d576a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWebProxy, IWebProxy interface [Windows Update Agent], IWebProxy interface [Windows Update Agent],described, wua.iwebproxy, wuapi/IWebProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWebProxy
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWebProxy interface


## -description


Contains the HTTP proxy settings.
<div class="alert"><b>Important</b>  This interface is not supported on Windows 10 and Windows Server 2016. See the remarks for more details.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebProxy</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWebProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWebProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eeb4418-d9fe-41b8-97c9-cafe18aab528">PromptForCredentials</a>
</td>
<td align="left" width="63%">
Prompts the user for the password to use for proxy authentication.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36ee1771-cfa6-4fa0-924b-69dbd57b1ad4">PromptForCredentialsFromHwnd</a>
</td>
<td align="left" width="63%">
Prompts the user for the password to use for proxy authentication.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59b500f1-2015-4f72-9be5-c2f57462dff0">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password to submit to the proxy server for authentication.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebProxy</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt427295">Address</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the address and the decimal port number of the proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cd222133-e44b-453a-9fbf-72f609cb2d4b">AutoDetect</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether <b>IWebProxy</b>  automatically detects proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a93742d2-73ce-4e7b-a000-592fd588cb1f">BypassList</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a collection of addresses that do not use the proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/541626ca-0b68-41cd-8f20-5ffd034fc878">BypassProxyOnLocal</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether local addresses  bypass the proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/daa1a276-e03c-448c-8572-3bec9151bcb7">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the <b>WebProxy</b> object is read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997357">UserName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the user name to submit to the proxy server for authentication.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the WebProxy coclass. Use the Microsoft.Update.WebProxy program identifier to create the object.

<div class="alert"><b>Important</b>  This interface is not supported on Windows 10 and Windows Server 2016. To configure proxy settings on  these operating systems (including proxy settings for  Windows Update Agent), use the  <b>Proxy</b> page of the <b>Network &amp; Internet</b> section in <b>Settings</b>. You can optionally use a <a href="https://en.wikipedia.org/wiki/Proxy_auto-config">proxy auto-config script</a> to apply settings. If you configure proxy settings, be sure to allow access to the domains used by Windows Update listed in <a href="https://support.microsoft.com/help/3084568/can-t-download-updates-from-windows-update-from-behind-a-firewall-or-p">this article</a>.</div>
<div> </div>


