---
UID: NN:ocidl.IOleInPlaceSiteEx
title: IOleInPlaceSiteEx
author: windows-sdk-content
description: Provides an additional set of activation and deactivation notification methods that enable an object to avoid unnecessary flashing on the screen when the object is activated and deactivated.
old-location: com\ioleinplacesiteex.htm
old-project: com
ms.assetid: d93e6d23-7867-43e4-8ab9-efe609362c18
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleInPlaceSiteEx, IOleInPlaceSiteEx interface [COM], IOleInPlaceSiteEx interface [COM],described, _ole_ioleinplacesiteex, com.ioleinplacesiteex, ocidl/IOleInPlaceSiteEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceSiteEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleInPlaceSiteEx interface


## -description


Provides an additional set of activation and deactivation notification methods that enable an object to avoid unnecessary flashing on the screen when the object is activated and deactivated.

When an object is activated, it does not know if its visual display is already correct. When the object is deactivated, the container does not know if the visual display is correct. To avoid a redraw and the associated screen flicker in both cases, the container can provide this extension to <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceSiteEx</b> interface inherits from <b>IOleInPlaceSite</b>. <b>IOleInPlaceSiteEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceSiteEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11c96c79-9884-4bac-828b-53ac4de65182">OnInPlaceActivateEx</a>
</td>
<td align="left" width="63%">
Called by the embedded object to determine whether it needs to redraw itself upon activation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3c68b46-adca-4f8d-86c2-075b72f7c656">OnInPlaceDeactivateEx</a>
</td>
<td align="left" width="63%">
Notifies the container whether the object needs to be redrawn upon deactivation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60baefc0-eaf6-4d73-975c-987a7720955b">RequestUIActivate</a>
</td>
<td align="left" width="63%">
Notifies the container that the object is about to enter the UI-active state.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

