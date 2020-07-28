---
UID: NN:winsatcominterfacei.IProvideWinSATVisuals
title: IProvideWinSATVisuals (winsatcominterfacei.h)
description: Retrieves elements that can be used in a user interface to graphically represent the WinSAT assessment.
helpviewer_keywords: ["IProvideWinSATVisuals","IProvideWinSATVisuals interface [WinSAT]","IProvideWinSATVisuals interface [WinSAT]","described","winsat.iprovidewinsatvisuals","winsatcominterfacei/IProvideWinSATVisuals"]
old-location: winsat\iprovidewinsatvisuals.htm
tech.root: WinSAT
ms.assetid: 9e8d2490-9d48-4512-b5f0-5c2f9cdeb287
ms.date: 12/05/2018
ms.keywords: IProvideWinSATVisuals, IProvideWinSATVisuals interface [WinSAT], IProvideWinSATVisuals interface [WinSAT],described, winsat.iprovidewinsatvisuals, winsatcominterfacei/IProvideWinSATVisuals
f1_keywords:
- winsatcominterfacei/IProvideWinSATVisuals
dev_langs:
- c++
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: Winsatapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Winsatapi.dll
api_name:
- IProvideWinSATVisuals
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProvideWinSATVisuals interface


## -description


<p class="CCE_Message">[IProvideWinSATVisuals may be altered or unavailable for releases after Windows 8.1.]

Retrieves elements that can be used in a user interface to graphically represent the WinSAT assessment.

To retrieve this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CProvideWinSATVisuals) as the class identifier and __uuidof(IProvideWinSATVisuals) as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideWinSATVisuals</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProvideWinSATVisuals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProvideWinSATVisuals</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap">get_Bitmap</a>
</td>
<td align="left" width="63%">
Retrieves a bitmap for the WinSAT base score.

</td>
</tr>
</table> 

