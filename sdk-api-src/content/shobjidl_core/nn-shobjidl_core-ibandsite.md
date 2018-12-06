---
UID: NN:shobjidl_core.IBandSite
title: IBandSite
author: windows-sdk-content
description: Exposes methods that control band objects.
old-location: shell\IBandSite.htm
tech.root: shell
ms.assetid: d7893136-a1a3-4c4b-b8f3-e4679710d827
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBandSite, IBandSite interface [Windows Shell], IBandSite interface [Windows Shell],described, _win32_IBandSite, shell.IBandSite, shobjidl_core/IBandSite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shldisp.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IBandSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandSite interface


## -description


Exposes methods that control band objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBandSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBandSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBandSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a954aaf2-f862-4aea-8643-a5b453a8d8ee">AddBand</a>
</td>
<td align="left" width="63%">
Adds a band to a band site object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d92ead78-9d58-48fe-ad93-33b2dbcbda68">EnumBands</a>
</td>
<td align="left" width="63%">
Enumerates the bands in a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6eba36d-5fc8-4b79-8129-1e07c5cc5b5f">GetBandObject</a>
</td>
<td align="left" width="63%">
Gets a specified band object from a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5831de51-f785-430e-b7e6-f1f40a83357b">GetBandSiteInfo</a>
</td>
<td align="left" width="63%">
Gets information about a band in the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0618ad7d-4e8f-4fbf-ab64-2b1c0d42158c">QueryBand</a>
</td>
<td align="left" width="63%">
Gets information about a band in a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5af20633-fab4-4fda-84c9-6bbdb9d588ec">RemoveBand</a>
</td>
<td align="left" width="63%">
Removes a band from the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2658a49d-d60f-483b-bbe1-e1390e9dc35e">SetBandSiteInfo</a>
</td>
<td align="left" width="63%">
Sets information about the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d327f0fe-7d61-4edd-aff3-f4507763d751">SetBandState</a>
</td>
<td align="left" width="63%">
Set the state of a band in the band site.

</td>
</tr>
</table> 


## -remarks



<b>IBandSite</b> is used to host band objects, such as <a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>.




## -see-also




<a href="https://msdn.microsoft.com/4bf46b3f-f833-42e0-baf7-21bfa9e6d890">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>



<a href="https://msdn.microsoft.com/f90efe85-78af-40c3-aea4-ed8818b04686">MenuBandSite</a>
 

 

