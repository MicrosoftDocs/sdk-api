---
UID: NN:qnetwork.IAMMediaContent
title: IAMMediaContent
author: windows-sdk-content
description: The IAMMediaContent interface retrieves metadata from a stream.
old-location: dshow\iammediacontent.htm
tech.root: DirectShow
ms.assetid: bd9cc96d-9664-41f3-9d4f-e5bdb1cb8d09
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMMediaContent, IAMMediaContent interface [DirectShow], IAMMediaContent interface [DirectShow],described, IAMMediaContentInterface, dshow.iammediacontent, qnetwork/IAMMediaContent
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
 - IAMMediaContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaContent interface


## -description



The <b>IAMMediaContent</b> interface retrieves metadata from a stream. Applications can use this interface to retrieve information encoded into a stream, such as the author, title, and copyright. This interface is exposed by the <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter and the <a href="https://msdn.microsoft.com/abadf37f-2876-496d-90e7-77c3475a0064">MPEG-1 Stream Splitter</a> filter.

Depending on the stream type, a filter might support a subset of the methods on this interface. For example, the AVI Splitter retrieves the copyright, author name, and title from INFO chunks in the AVI file. The remaining methods return <b> E_NOTIMPL</b>.

<div class="alert"><b>Note</b>  Windows Media Player does not use this interface to display metadata.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaContent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMMediaContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49ccb07c-1f20-47e9-a05b-f8f3b77acc99">get_AuthorName</a>
</td>
<td align="left" width="63%">
Gets the author name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fd88d09-79bf-45c6-93b4-1f57752ed1cd">get_BaseURL</a>
</td>
<td align="left" width="63%">
Gets a base URL for the related web content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63dc869-6b95-4923-80a6-22b5d8b81fa0">get_Copyright</a>
</td>
<td align="left" width="63%">
Gets copyright information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc0c14f3-2764-4897-8ddb-ed1146d98597">get_Description</a>
</td>
<td align="left" width="63%">
Gets a description of the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/249f06ad-1571-4259-aaae-d0bc8208b9e5">get_LogoIconURL</a>
</td>
<td align="left" width="63%">
Gets a URL for the logo icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a17c080-49a9-4b0b-8d94-054ad53b95b8">get_LogoURL</a>
</td>
<td align="left" width="63%">
Gets a URL for the logo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae456ce2-4df8-4a36-88f5-526acb722bda">get_MoreInfoBannerImage</a>
</td>
<td align="left" width="63%">
Gets an image for a related-information banner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc820849-cab2-4770-bdb2-6c4b32f3cc56">get_MoreInfoBannerURL</a>
</td>
<td align="left" width="63%">
Gets a URL for a related-information banner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a511c86-0a3a-48d3-8a3a-2ab52ff7dcea">get_MoreInfoText</a>
</td>
<td align="left" width="63%">
Gets additional information as text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8efaa0b9-09c1-4434-a992-6290fc388cb2">get_MoreInfoURL</a>
</td>
<td align="left" width="63%">
Gets a URL for additional information about the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eeb1356-23f5-48dc-be71-062f1501d163">get_Rating</a>
</td>
<td align="left" width="63%">
Gets the rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60543438-9547-44fe-8468-baee03d6ebc9">get_Title</a>
</td>
<td align="left" width="63%">
Gets the title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e632f99e-7e08-4dfa-9f4e-5f09d9d77eb8">get_WatermarkURL</a>
</td>
<td align="left" width="63%">
Gets a URL for the watermark.

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
 

 

