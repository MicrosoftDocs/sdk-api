---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWICStreamProvider interface


## -description


Exposes methods for a stream provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICStreamProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICStreamProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICStreamProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/244d4335-ee5f-434e-8d0b-4ba5d984b207">GetPersistOptions</a>
</td>
<td align="left" width="63%">
Gets the persist options used when initializing the component with a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb88bc8d-4f92-4645-9d11-ee9200f11aaf">GetPreferredVendorGUID</a>
</td>
<td align="left" width="63%">
Gets the preferred vendor GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c86e507b-0b1d-4de0-8af5-c46d7870fb09">GetStream</a>
</td>
<td align="left" width="63%">
Gets the stream held by the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ee9b2a-b979-4009-b4e6-e2e39548976d">RefreshStream</a>
</td>
<td align="left" width="63%">
Informs the component that the content of the stream it's holding onto may have changed. The component should respond by dirtying any cached information from the stream.

</td>
</tr>
</table> 

