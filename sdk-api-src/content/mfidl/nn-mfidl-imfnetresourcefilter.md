---
UID: NN:mfidl.IMFNetResourceFilter
title: IMFNetResourceFilter (mfidl.h)
author: windows-sdk-content
description: Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.
old-location: mf\imfnetresourcefilter.htm
tech.root: medfound
ms.assetid: AC8FBD93-B39B-4530-8475-275D3D0DA512
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter, IMFNetResourceFilter interface [Media Foundation], IMFNetResourceFilter interface [Media Foundation],described, mf.imfnetresourcefilter, mfidl/IMFNetResourceFilter
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFNetResourceFilter"
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - mfidl.h
api_name:
 - IMFNetResourceFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetResourceFilter interface


## -description


Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetResourceFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetResourceFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetResourceFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetresourcefilter-onredirect">OnRedirect</a>
</td>
<td align="left" width="63%">
Called when the byte stream redirects to a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetresourcefilter-onsendingrequest">OnSendingRequest</a>
</td>
<td align="left" width="63%">
Called when the byte stream requests a URL.

</td>
</tr>
</table> 


## -remarks



To set the callback interface:

<ol>
<li>Query the byte stream object for the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown">IMFAttributes::SetUnknown</a> to set the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfnetsource-resource-filter">MFNETSOURCE_RESOURCE_FILTER</a> attribute.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

