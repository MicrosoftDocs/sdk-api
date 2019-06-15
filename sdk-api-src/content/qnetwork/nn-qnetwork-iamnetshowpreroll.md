---
UID: NN:qnetwork.IAMNetShowPreroll
title: IAMNetShowPreroll (qnetwork.h)
author: windows-sdk-content
description: The IAMNetShowPreroll interface sets and retrieves the preroll settings for the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface. The filter's default preroll time is five seconds.
old-location: dshow\iamnetshowpreroll.htm
tech.root: DirectShow
ms.assetid: 13478678-00de-48e6-b9e7-fd47db423290
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMNetShowPreroll, IAMNetShowPreroll interface [DirectShow], IAMNetShowPreroll interface [DirectShow],described, IAMNetShowPrerollInterface, dshow.iamnetshowpreroll, qnetwork/IAMNetShowPreroll
ms.topic: interface
f1_keywords: ["qnetwork/IAMNetShowPreroll"]
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
 - IAMNetShowPreroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowPreroll interface


## -description



The <code>IAMNetShowPreroll</code> interface sets and retrieves the preroll settings for the legacy Windows Media Player 6.4 source filter. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter implements this interface. The filter's default preroll time is five seconds.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowPreroll</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMNetShowPreroll</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMNetShowPreroll</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowpreroll-get_preroll">get_Preroll</a>
</td>
<td align="left" width="63%">
Queries whether the filter is currently prerolling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowpreroll-put_preroll">put_Preroll</a>
</td>
<td align="left" width="63%">
Specifies whether the filter should start prerolling.

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
 

 

