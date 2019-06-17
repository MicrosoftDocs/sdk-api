---
UID: NN:mfidl.IMFContentEnabler
title: IMFContentEnabler (mfidl.h)
author: windows-sdk-content
description: Implements one step that must be performed for the user to access media content.
old-location: mf\imfcontentenabler.htm
tech.root: medfound
ms.assetid: 45d02bd0-1104-47ec-8559-8cc51590fc62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 45d02bd0-1104-47ec-8559-8cc51590fc62, IMFContentEnabler, IMFContentEnabler interface [Media Foundation], IMFContentEnabler interface [Media Foundation],described, mf.imfcontentenabler, mfidl/IMFContentEnabler
ms.topic: interface
f1_keywords: ["mfidl/IMFContentEnabler"]
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
ms.custom: 19H1
---

# IMFContentEnabler interface


## -description


Implements one step that must be performed for the user to access media content. For example, the steps might be individualization followed by license acquisition. Each of these steps would be encapsulated by a content enabler object that exposes the <b>IMFContentEnabler</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentEnabler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFContentEnabler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable">AutomaticEnable</a>
</td>
<td align="left" width="63%">
Performs a content enabling action without any user interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata">GetEnableData</a>
</td>
<td align="left" width="63%">
Retrieves the data for a manual content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabletype">GetEnableType</a>
</td>
<td align="left" width="63%">
Retrieves the type of operation that this content enabler performs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl">GetEnableURL</a>
</td>
<td align="left" width="63%">
Retrieves a URL for performing a manual content enabling action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported">IsAutomaticSupported</a>
</td>
<td align="left" width="63%">
Queries whether the content enabler can perform all of its actions automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable">MonitorEnable</a>
</td>
<td align="left" width="63%">
Requests notification when the enabling action is completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

