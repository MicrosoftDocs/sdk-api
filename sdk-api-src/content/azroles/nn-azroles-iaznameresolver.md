---
UID: NN:azroles.IAzNameResolver
title: IAzNameResolver (azroles.h)
description: Translates security identifiers (SIDs) into principal display names.helpviewer_keywords: ["IAzNameResolver","IAzNameResolver interface [Security]","IAzNameResolver interface [Security]","described","azroles/IAzNameResolver","security.iaznameresolver"]
old-location: security\iaznameresolver.htm
tech.root: SecAuthZ
ms.assetid: 9426a623-cefc-43ed-9987-77802fce1a78
ms.date: 12/05/2018
ms.keywords: IAzNameResolver, IAzNameResolver interface [Security], IAzNameResolver interface [Security],described, azroles/IAzNameResolver, security.iaznameresolver
f1_keywords:
- azroles/IAzNameResolver
dev_langs:
- c++
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzNameResolver
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzNameResolver interface


## -description


The <b>IAzNameResolver</b> interface translates <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) into principal display names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzNameResolver</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzNameResolver</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzNameResolver</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iaznameresolver-namefromsid">NameFromSid</a>
</td>
<td align="left" width="63%">
Gets the display name that corresponds to the specified SID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iaznameresolver-namesfromsids">NamesFromSids</a>
</td>
<td align="left" width="63%">
Gets the display names that correspond to the specified SIDs.

</td>
</tr>
</table> 

