---
UID: NN:textserv.IRichEditUiaInformation
title: IRichEditUiaInformation (textserv.h)
description: Provides Microsoft UI Automation accessibility information about a windowless rich edit control.
helpviewer_keywords: ["IRichEditUiaInformation","IRichEditUiaInformation interface [Windows Controls]","IRichEditUiaInformation interface [Windows Controls]","described","controls.irichedituiainformation","textserv/IRichEditUiaInformation"]
old-location: controls\irichedituiainformation.htm
tech.root: Controls
ms.assetid: BEED428C-6C88-45A8-948C-77288B817C49
ms.date: 12/05/2018
ms.keywords: IRichEditUiaInformation, IRichEditUiaInformation interface [Windows Controls], IRichEditUiaInformation interface [Windows Controls],described, controls.irichedituiainformation, textserv/IRichEditUiaInformation
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditUiaInformation
 - textserv/IRichEditUiaInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditUiaInformation
---

# IRichEditUiaInformation interface


## -description

Provides Microsoft UI Automation accessibility information about a windowless rich edit control.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRichEditUiaInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRichEditUiaInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRichEditUiaInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/textserv/nf-textserv-irichedituiainformation-getboundaryrectangle">GetBoundaryRectangle</a>
</td>
<td align="left" width="63%">
Retrieves the bounding rectangle of a windowless rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/textserv/nf-textserv-irichedituiainformation-isvisible">IsVisible</a>
</td>
<td align="left" width="63%">
Indicates whether a windowless rich edit control is currently visible.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textserv/nn-textserv-irichedituiaoverrides">IRichEditUiaOverrides</a>



<a href="/windows/desktop/api/textserv/nn-textserv-iricheditwindowlessaccessibility">IRicheditWindowlessAccessibility</a>