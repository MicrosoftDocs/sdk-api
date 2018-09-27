---
UID: NN:qnetwork.IAMNetworkStatus
title: IAMNetworkStatus
author: windows-sdk-content
description: The IAMNetworkStatus interface reports the quality of the network connection for the legacy Windows Media Player 6.4 source filter.
old-location: dshow\iamnetworkstatus.htm
tech.root: DirectShow
ms.assetid: 51d56b76-f9fc-44e1-88f0-d35d861a4697
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAMNetworkStatus, IAMNetworkStatus interface [DirectShow], IAMNetworkStatus interface [DirectShow],described, IAMNetworkStatusInterface, dshow.iamnetworkstatus, qnetwork/IAMNetworkStatus
ms.prod: windows
ms.technology: windows-sdk
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
 - IAMNetworkStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetworkStatus interface


## -description



The <code>IAMNetworkStatus</code> interface reports the quality of the network connection for the legacy Windows Media Player 6.4 source filter. The <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter implements this interface. It enables clients to retrieve information about the quality of the network connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetworkStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMNetworkStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMNetworkStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82c1994b-9326-48a7-8ff5-2b2df274b3e2">get_BufferingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times the network source has buffered the data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76276bdc-1f19-4fb9-8ae9-1edeb5639741">get_BufferingProgress</a>
</td>
<td align="left" width="63%">
Retrieves the buffering progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/578fe82b-0c87-47ea-9600-91d68f4c733f">get_IsBroadcast</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the current clip is a broadcast clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/814a2ffa-c7f3-47e6-8956-4a705b394469">get_LostPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of lost packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9437489d-87bf-45d4-82f3-22e8adb4df54">get_ReceivedPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of received packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c80f874-c176-4e52-acc9-26c10fac08d9">get_ReceptionQuality</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the reception quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8362d52-ed20-444e-86ab-26c9eac3087c">get_RecoveredPackets</a>
</td>
<td align="left" width="63%">
Retrieves the number of recovered packets.

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
 

 

