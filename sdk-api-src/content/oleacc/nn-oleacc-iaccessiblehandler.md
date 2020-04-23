---
UID: NN:oleacc.IAccessibleHandler
title: IAccessibleHandler (oleacc.h)
description: Exposes a method that retrieves an accessible element from an object ID.helpviewer_keywords: ["IAccessibleHandler","IAccessibleHandler interface [Windows Accessibility]","IAccessibleHandler interface [Windows Accessibility]","described","msaa.iaccessiblehandler","oleacc/IAccessibleHandler","winauto.iaccessiblehandler"]
old-location: winauto\iaccessiblehandler.htm
tech.root: WinAuto
ms.assetid: 1b6b2c02-f3b5-4a8a-9388-b3833cd0cd44
ms.date: 12/05/2018
ms.keywords: IAccessibleHandler, IAccessibleHandler interface [Windows Accessibility], IAccessibleHandler interface [Windows Accessibility],described, msaa.iaccessiblehandler, oleacc/IAccessibleHandler, winauto.iaccessiblehandler
f1_keywords:
- oleacc/IAccessibleHandler
dev_langs:
- c++
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- oleacc.h
api_name:
- IAccessibleHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessibleHandler interface


## -description


<p class="CCE_Message">[<b>IAccessibleHandler</b> is deprecated and should not be used.]

Exposes a method that retrieves an accessible element from an object ID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessibleHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid">AccessibleObjectFromID</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer 
	 for the element associated with an accessible object.

</td>
</tr>
</table> 

