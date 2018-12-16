---
UID: NN:qnetwork.IAMNetShowConfig
title: IAMNetShowConfig
author: windows-sdk-content
description: The IAMNetShowConfig interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
old-location: dshow\iamnetshowconfig.htm
tech.root: DirectShow
ms.assetid: 611b43dc-7f6d-404e-90a4-b109b9475fb6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMNetShowConfig, IAMNetShowConfig interface [DirectShow], IAMNetShowConfig interface [DirectShow],described, IAMNetShowConfigInterface, dshow.iamnetshowconfig, qnetwork/IAMNetShowConfig
ms.topic: interface
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetShowConfig interface


## -description



The <code>IAMNetShowConfig</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMNetShowConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMNetShowConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319697(v=VS.85).aspx">get_BufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the buffering time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319698(v=VS.85).aspx">get_EnableAutoProxy</a>
</td>
<td align="left" width="63%">
Queries whether the control or filter should use the browser's proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319699(v=VS.85).aspx">get_EnableHTTP</a>
</td>
<td align="left" width="63%">
Queries whether HTTP-type streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319700(v=VS.85).aspx">get_EnableMulticast</a>
</td>
<td align="left" width="63%">
Queries whether multicast-type streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319701(v=VS.85).aspx">get_EnableTCP</a>
</td>
<td align="left" width="63%">
Queries whether TCP-based streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319702(v=VS.85).aspx">get_EnableUDP</a>
</td>
<td align="left" width="63%">
Queries whether UDP-based streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319703(v=VS.85).aspx">get_FixedUDPPort</a>
</td>
<td align="left" width="63%">
Retrieves the fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319704(v=VS.85).aspx">get_HTTPProxyHost</a>
</td>
<td align="left" width="63%">
Retrieves the HTTP address of the proxy host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319705(v=VS.85).aspx">get_HTTPProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the HTTP proxy port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319706(v=VS.85).aspx">get_UseFixedUDPPort</a>
</td>
<td align="left" width="63%">
Queries whether the filter should use the fixed UDP port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319707(v=VS.85).aspx">get_UseHTTPProxy</a>
</td>
<td align="left" width="63%">
Queries whether the filter should use the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319708(v=VS.85).aspx">put_BufferingTime</a>
</td>
<td align="left" width="63%">
Specifies the buffering time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319709(v=VS.85).aspx">put_EnableAutoProxy</a>
</td>
<td align="left" width="63%">
Specifies whether the control or filter should use the browser's proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319710(v=VS.85).aspx">put_EnableHTTP</a>
</td>
<td align="left" width="63%">
Enables or disables HTTP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319711(v=VS.85).aspx">put_EnableMulticast</a>
</td>
<td align="left" width="63%">
Enables or disables multicast-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319712(v=VS.85).aspx">put_EnableTCP</a>
</td>
<td align="left" width="63%">
Enables or disables TCP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319713(v=VS.85).aspx">put_EnableUDP</a>
</td>
<td align="left" width="63%">
Enables or disables UDP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319714(v=VS.85).aspx">put_FixedUDPPort</a>
</td>
<td align="left" width="63%">
Specifies the fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319715(v=VS.85).aspx">put_HTTPProxyHost</a>
</td>
<td align="left" width="63%">
Specifies the address of the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319716(v=VS.85).aspx">put_HTTPProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the port for the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319717(v=VS.85).aspx">put_UseFixedUDPPort</a>
</td>
<td align="left" width="63%">
Specifies whether to use a fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319718(v=VS.85).aspx">put_UseHTTPProxy</a>
</td>
<td align="left" width="63%">
Specifies whether to use an HTTP proxy server.

</td>
</tr>
</table> 


## -remarks



To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

