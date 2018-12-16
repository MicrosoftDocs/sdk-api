---
UID: NN:qnetwork.IAMChannelInfo
title: IAMChannelInfo
author: windows-sdk-content
description: The IAMChannelInfo interface gets and sets channel information for Windows Media Station (.nsc) files.This interface is exposed by the Windows Media Source filter only when the filter is reading Windows Media Station (.nsc) files.
old-location: dshow\iamchannelinfo.htm
tech.root: DirectShow
ms.assetid: 779d1c0a-f838-4d02-8254-d66916d3b790
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMChannelInfo, IAMChannelInfo interface [DirectShow], IAMChannelInfo interface [DirectShow],described, IAMChannelInfoInterface, dshow.iamchannelinfo, qnetwork/IAMChannelInfo
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
 - IAMChannelInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMChannelInfo interface


## -description



The <b>IAMChannelInfo</b> interface gets and sets channel information for Windows Media Station (.nsc) files.

This interface is exposed by the <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter only when the filter is reading Windows Media Station (.nsc) files. The Windows Media Source filter uses .nsc files to get the information it needs to receive multicast content over the Internet. These files contain information such as stream location and rollover URL, as well as descriptive information about the station.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMChannelInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMChannelInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMChannelInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389155(v=VS.85).aspx">get_ChannelDescription</a>
</td>
<td align="left" width="63%">
Gets the description of the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389156(v=VS.85).aspx">get_ChannelName</a>
</td>
<td align="left" width="63%">
Gets the channel name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389157(v=VS.85).aspx">get_ChannelURL</a>
</td>
<td align="left" width="63%">
Gets the channel URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389158(v=VS.85).aspx">get_ContactAddress</a>
</td>
<td align="left" width="63%">
Gets the contact address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389159(v=VS.85).aspx">get_ContactEmail</a>
</td>
<td align="left" width="63%">
Gets the contact email address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389160(v=VS.85).aspx">get_ContactPhone</a>
</td>
<td align="left" width="63%">
Gets the contact phone number.

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



<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

