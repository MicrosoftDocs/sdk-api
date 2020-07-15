---
UID: NN:textserv.IRicheditUiaOverrides
title: IRicheditUiaOverrides (textserv.h)
description: Enables the host container of a windowless rich edit control to override the control's Microsoft UI Automation accessibility properties.
helpviewer_keywords: ["IRicheditUiaOverrides","IRicheditUiaOverrides interface [Windows Controls]","IRicheditUiaOverrides interface [Windows Controls]","described","controls.irichedituiaoverrides","textserv/IRicheditUiaOverrides"]
old-location: controls\irichedituiaoverrides.htm
tech.root: Controls
ms.assetid: 2590002F-A6B0-4AA7-A54C-A5AB5304D9FA
ms.date: 12/05/2018
ms.keywords: IRicheditUiaOverrides, IRicheditUiaOverrides interface [Windows Controls], IRicheditUiaOverrides interface [Windows Controls],described, controls.irichedituiaoverrides, textserv/IRicheditUiaOverrides
f1_keywords:
- textserv/IRicheditUiaOverrides
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- IRicheditUiaOverrides
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRicheditUiaOverrides interface


## -description


Enables the host  container of a windowless rich edit control to override the control's Microsoft UI Automation accessibility properties.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRicheditUiaOverrides</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRicheditUiaOverrides</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRicheditUiaOverrides</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-irichedituiaoverrides-getpropertyoverridevalue">GetPropertyOverrideValue</a>
</td>
<td align="left" width="63%">
Retrieves the host container's override value for the specified UI Automation accessibility property of a windowless rich edit control.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nn-textserv-irichedituiainformation">IRichEditUiaInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nn-textserv-iricheditwindowlessaccessibility">IRicheditWindowlessAccessibility</a>
 

 

