---
UID: NN:mfidl.IMFContentEnabler
title: IMFContentEnabler
author: windows-sdk-content
description: Implements one step that must be performed for the user to access media content.
old-location: mf\imfcontentenabler.htm
tech.root: medfound
ms.assetid: 45d02bd0-1104-47ec-8559-8cc51590fc62
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 45d02bd0-1104-47ec-8559-8cc51590fc62, IMFContentEnabler, IMFContentEnabler interface [Media Foundation], IMFContentEnabler interface [Media Foundation],described, mf.imfcontentenabler, mfidl/IMFContentEnabler
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentEnabler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentEnabler interface


## -description


Implements one step that must be performed for the user to access media content. For example, the steps might be individualization followed by license acquisition. Each of these steps would be encapsulated by a content enabler object that exposes the <b>IMFContentEnabler</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentEnabler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFContentEnabler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFContentEnabler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7be4c32f-d116-4a08-857f-1a59b5ccfb12">AutomaticEnable</a>
</td>
<td align="left" width="63%">
Performs a content enabling action without any user interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e273b702-1f42-4aeb-9259-778d3f206682">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1859037-7a33-4943-8ca9-6782fc8b0b92">GetEnableData</a>
</td>
<td align="left" width="63%">
Retrieves the data for a manual content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fe597d8-788c-48c4-a21a-0b91a890710f">GetEnableType</a>
</td>
<td align="left" width="63%">
Retrieves the type of operation that this content enabler performs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a44216d-36e5-4b5c-9585-5297d5e429f9">GetEnableURL</a>
</td>
<td align="left" width="63%">
Retrieves a URL for performing a manual content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/144470ce-2849-4464-8596-fac216529145">IsAutomaticSupported</a>
</td>
<td align="left" width="63%">
Queries whether the content enabler can perform all of its actions automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78fc4a17-f58c-4654-b37e-6b988848ff0d">MonitorEnable</a>
</td>
<td align="left" width="63%">
Requests notification when the enabling action is completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

