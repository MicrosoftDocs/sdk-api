---
UID: NN:mfidl.IMFNetResourceFilter
title: IMFNetResourceFilter
author: windows-sdk-content
description: Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.
old-location: mf\imfnetresourcefilter.htm
tech.root: medfound
ms.assetid: AC8FBD93-B39B-4530-8475-275D3D0DA512
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFNetResourceFilter, IMFNetResourceFilter interface [Media Foundation], IMFNetResourceFilter interface [Media Foundation],described, mf.imfnetresourcefilter, mfidl/IMFNetResourceFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetResourceFilter interface


## -description


Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetResourceFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetResourceFilter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/418EA3E0-9732-43B7-BF80-A85ECB7A9485">OnRedirect</a>
</td>
<td align="left" width="63%">
Called when the byte stream redirects to a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4FE6BBE8-A8EC-4304-BC4B-4D49F8EADC25">OnSendingRequest</a>
</td>
<td align="left" width="63%">
Called when the byte stream requests a URL.

</td>
</tr>
</table> 


## -remarks



To set the callback interface:

<ol>
<li>Query the byte stream object for the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/da0c3d59-07c4-4431-a137-8655ddbf6258">IMFAttributes::SetUnknown</a> to set the <a href="https://msdn.microsoft.com/C035B4AD-CF99-4A4F-9384-F80A3620BD27">MFNETSOURCE_RESOURCE_FILTER</a> attribute.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

