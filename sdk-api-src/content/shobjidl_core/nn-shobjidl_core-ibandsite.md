---
UID: NN:shobjidl_core.IBandSite
title: IBandSite (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that control band objects.
old-location: shell\IBandSite.htm
tech.root: shell
ms.assetid: d7893136-a1a3-4c4b-b8f3-e4679710d827
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBandSite, IBandSite interface [Windows Shell], IBandSite interface [Windows Shell],described, _win32_IBandSite, shell.IBandSite, shobjidl_core/IBandSite
ms.topic: interface
f1_keywords: ["shobjidl_core/IBandSite"]
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
ms.custom: 19H1
---

# IBandSite interface


## -description


Exposes methods that control band objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBandSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBandSite</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-addband">AddBand</a>
</td>
<td align="left" width="63%">
Adds a band to a band site object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-enumbands">EnumBands</a>
</td>
<td align="left" width="63%">
Enumerates the bands in a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandobject">GetBandObject</a>
</td>
<td align="left" width="63%">
Gets a specified band object from a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo">GetBandSiteInfo</a>
</td>
<td align="left" width="63%">
Gets information about a band in the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-queryband">QueryBand</a>
</td>
<td align="left" width="63%">
Gets information about a band in a band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-removeband">RemoveBand</a>
</td>
<td align="left" width="63%">
Removes a band from the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo">SetBandSiteInfo</a>
</td>
<td align="left" width="63%">
Sets information about the band site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandstate">SetBandState</a>
</td>
<td align="left" width="63%">
Set the state of a band in the band site.

</td>
</tr>
</table> 


## -remarks



<b>IBandSite</b> is used to host band objects, such as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/mandatory-user-profiles">MenuBandSite</a>
 

 

