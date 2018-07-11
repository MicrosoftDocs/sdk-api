---
UID: NN:qnetwork.IAMChannelInfo
title: IAMChannelInfo
author: windows-sdk-content
description: The IAMChannelInfo interface gets and sets channel information for Windows Media Station (.nsc) files.This interface is exposed by the Windows Media Source filter only when the filter is reading Windows Media Station (.nsc) files.
old-location: dshow\iamchannelinfo.htm
old-project: DirectShow
ms.assetid: 779d1c0a-f838-4d02-8254-d66916d3b790
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMChannelInfo, IAMChannelInfo interface [DirectShow], IAMChannelInfo interface [DirectShow],described, IAMChannelInfoInterface, dshow.iamchannelinfo, qnetwork/IAMChannelInfo
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMChannelInfo interface


## -description



The <b>IAMChannelInfo</b> interface gets and sets channel information for Windows Media Station (.nsc) files.

This interface is exposed by the <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter only when the filter is reading Windows Media Station (.nsc) files. The Windows Media Source filter uses .nsc files to get the information it needs to receive multicast content over the Internet. These files contain information such as stream location and rollover URL, as well as descriptive information about the station.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMChannelInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMChannelInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c39b15af-0766-4512-9720-4cdaef6120ba">get_ChannelDescription</a>
</td>
<td align="left" width="63%">
Gets the description of the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cf4f8aa-d6aa-46bd-83b1-fba762fbb8bb">get_ChannelName</a>
</td>
<td align="left" width="63%">
Gets the channel name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27e1a315-db95-4f24-94b6-b10023e61e7a">get_ChannelURL</a>
</td>
<td align="left" width="63%">
Gets the channel URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b94ccc71-92d1-4c1a-b34a-c34e6ea7bd91">get_ContactAddress</a>
</td>
<td align="left" width="63%">
Gets the contact address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ab9fc0-1370-44a1-95c8-6592c374d8d6">get_ContactEmail</a>
</td>
<td align="left" width="63%">
Gets the contact email address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5addbbb-a0f3-4dec-a347-9c69864a0615">get_ContactPhone</a>
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




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

