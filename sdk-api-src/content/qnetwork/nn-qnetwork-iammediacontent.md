---
UID: NN:qnetwork.IAMMediaContent
title: IAMMediaContent (qnetwork.h)
author: windows-sdk-content
description: The IAMMediaContent interface retrieves metadata from a stream.
old-location: dshow\iammediacontent.htm
tech.root: DirectShow
ms.assetid: bd9cc96d-9664-41f3-9d4f-e5bdb1cb8d09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMMediaContent, IAMMediaContent interface [DirectShow], IAMMediaContent interface [DirectShow],described, IAMMediaContentInterface, dshow.iammediacontent, qnetwork/IAMMediaContent
ms.topic: interface
f1_keywords: 
 - "qnetwork/IAMMediaContent"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaContent interface


## -description



The <b>IAMMediaContent</b> interface retrieves metadata from a stream. Applications can use this interface to retrieve information encoded into a stream, such as the author, title, and copyright. This interface is exposed by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter and the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-1-stream-splitter-filter">MPEG-1 Stream Splitter</a> filter.

Depending on the stream type, a filter might support a subset of the methods on this interface. For example, the AVI Splitter retrieves the copyright, author name, and title from INFO chunks in the AVI file. The remaining methods return <b> E_NOTIMPL</b>.

<div class="alert"><b>Note</b>  Windows Media Player does not use this interface to display metadata.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaContent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMMediaContent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_authorname">get_AuthorName</a>
</td>
<td align="left" width="63%">
Gets the author name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_baseurl">get_BaseURL</a>
</td>
<td align="left" width="63%">
Gets a base URL for the related web content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_copyright">get_Copyright</a>
</td>
<td align="left" width="63%">
Gets copyright information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Gets a description of the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_logoiconurl">get_LogoIconURL</a>
</td>
<td align="left" width="63%">
Gets a URL for the logo icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_logourl">get_LogoURL</a>
</td>
<td align="left" width="63%">
Gets a URL for the logo.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_moreinfobannerimage">get_MoreInfoBannerImage</a>
</td>
<td align="left" width="63%">
Gets an image for a related-information banner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_moreinfobannerurl">get_MoreInfoBannerURL</a>
</td>
<td align="left" width="63%">
Gets a URL for a related-information banner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_moreinfotext">get_MoreInfoText</a>
</td>
<td align="left" width="63%">
Gets additional information as text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_moreinfourl">get_MoreInfoURL</a>
</td>
<td align="left" width="63%">
Gets a URL for additional information about the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_rating">get_Rating</a>
</td>
<td align="left" width="63%">
Gets the rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_title">get_Title</a>
</td>
<td align="left" width="63%">
Gets the title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent-get_watermarkurl">get_WatermarkURL</a>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

