---
UID: NN:qnetwork.IAMMediaContent2
title: IAMMediaContent2 (qnetwork.h)
author: windows-sdk-content
description: The IAMMediaContent2 interface retrieves custom parameters and playlists from ASX files. This interface is not implemented by any default components in DirectShow.
old-location: dshow\iammediacontent2.htm
tech.root: DirectShow
ms.assetid: cf8381f2-2ef0-4169-8029-bce36bf3d6a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMMediaContent2, IAMMediaContent2 interface [DirectShow], IAMMediaContent2 interface [DirectShow],described, IAMMediaContent2Interface, dshow.iammediacontent2, qnetwork/IAMMediaContent2
ms.topic: interface
f1_keywords: 
 - "qnetwork/IAMMediaContent2"
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
 - IAMMediaContent2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaContent2 interface


## -description



The <code>IAMMediaContent2</code> interface retrieves custom parameters and playlists from ASX files. This interface is not implemented by any default components in DirectShow.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaContent2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMMediaContent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaContent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent2-get_mediaparameter">get_MediaParameter</a>
</td>
<td align="left" width="63%">
Retrieves the value of a custom parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent2-get_mediaparametername">get_MediaParameterName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a custom parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iammediacontent2-get_playlistcount">get_PlaylistCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of playlist entries.

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
 

 

