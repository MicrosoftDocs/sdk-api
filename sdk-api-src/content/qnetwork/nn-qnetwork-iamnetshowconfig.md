---
UID: NN:qnetwork.IAMNetShowConfig
title: IAMNetShowConfig
author: windows-driver-content
description: The IAMNetShowConfig interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
old-location: dshow\iamnetshowconfig.htm
old-project: DirectShow
ms.assetid: 611b43dc-7f6d-404e-90a4-b109b9475fb6
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMNetShowConfig, IAMNetShowConfig interface [DirectShow], IAMNetShowConfig interface [DirectShow],described, IAMNetShowConfigInterface, dshow.iamnetshowconfig, qnetwork/IAMNetShowConfig
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetShowConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAMNetShowConfig interface


## -description



The <code>IAMNetShowConfig</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowConfig</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAMNetShowConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8594f8dd-9545-4e6d-b1d7-9a278dcb4129">get_BufferingTime</a>
</td>
<td align="left" width="63%">
Retrieves the buffering time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7037f326-3320-4e4a-8f6f-feda1a306c2d">get_EnableAutoProxy</a>
</td>
<td align="left" width="63%">
Queries whether the control or filter should use the browser's proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29495a89-644f-4c55-a740-efb0cbf6d581">get_EnableHTTP</a>
</td>
<td align="left" width="63%">
Queries whether HTTP-type streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dae5c0ad-a41e-424c-a04d-69dbe7264143">get_EnableMulticast</a>
</td>
<td align="left" width="63%">
Queries whether multicast-type streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4282f84-e05b-407f-9425-0690783957c4">get_EnableTCP</a>
</td>
<td align="left" width="63%">
Queries whether TCP-based streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c689c9-34f6-49b2-bd3b-0f68a110c4f2">get_EnableUDP</a>
</td>
<td align="left" width="63%">
Queries whether UDP-based streaming is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0890d29b-540a-45ce-a5f0-04a2db517135">get_FixedUDPPort</a>
</td>
<td align="left" width="63%">
Retrieves the fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d73aefda-2c51-466a-b590-c8f189db4719">get_HTTPProxyHost</a>
</td>
<td align="left" width="63%">
Retrieves the HTTP address of the proxy host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a0325bb-83d6-4fbc-a513-0b6002013a60">get_HTTPProxyPort</a>
</td>
<td align="left" width="63%">
Retrieves the HTTP proxy port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a4b1f3b-c630-4820-a9d1-0e93f295b7f7">get_UseFixedUDPPort</a>
</td>
<td align="left" width="63%">
Queries whether the filter should use the fixed UDP port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d51676a-bf14-408c-bc8b-331ce11fc237">get_UseHTTPProxy</a>
</td>
<td align="left" width="63%">
Queries whether the filter should use the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60dea6f3-b45f-44a1-ba21-eb71206b2fb5">put_BufferingTime</a>
</td>
<td align="left" width="63%">
Specifies the buffering time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2746e4d9-3996-4b06-bbb9-7777de6d0202">put_EnableAutoProxy</a>
</td>
<td align="left" width="63%">
Specifies whether the control or filter should use the browser's proxy settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/162a581d-9697-4a6e-aedc-ec1ebc28a867">put_EnableHTTP</a>
</td>
<td align="left" width="63%">
Enables or disables HTTP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8415560c-0dc8-4d37-b584-9e278542cf15">put_EnableMulticast</a>
</td>
<td align="left" width="63%">
Enables or disables multicast-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e875901-7ccb-4aa5-b283-f75b791e85f1">put_EnableTCP</a>
</td>
<td align="left" width="63%">
Enables or disables TCP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2573573e-97e0-4ed4-b702-8c54ef47c5f4">put_EnableUDP</a>
</td>
<td align="left" width="63%">
Enables or disables UDP-based streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/461b3999-ee1f-4d2a-9ebc-38faf344eba0">put_FixedUDPPort</a>
</td>
<td align="left" width="63%">
Specifies the fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cd37fd4-3ce0-4b5c-9e2f-88c0e1845b2d">put_HTTPProxyHost</a>
</td>
<td align="left" width="63%">
Specifies the address of the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dada8684-66e7-4983-984a-589d48d167ba">put_HTTPProxyPort</a>
</td>
<td align="left" width="63%">
Specifies the port for the HTTP proxy server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7b0c118-0479-4f28-8e2f-6c143cde9ff0">put_UseFixedUDPPort</a>
</td>
<td align="left" width="63%">
Specifies whether to use a fixed UDP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4be1ca01-49c6-4b1e-8fb6-41e598fd157f">put_UseHTTPProxy</a>
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




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

