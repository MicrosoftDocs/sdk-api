---
UID: NN:imepad.IImeSpecifyApplets
title: IImeSpecifyApplets (imepad.h)
description: The IImeSpecifyApplets interface specifies methods called from the IImePad interface object to emulate the IImePadApplet interface.
helpviewer_keywords: ["IImeSpecifyApplets","IImeSpecifyApplets interface [Internationalization for Windows Applications]","IImeSpecifyApplets interface [Internationalization for Windows Applications]","described","imepad/IImeSpecifyApplets","intl.iimespecifyapplets"]
old-location: intl\iimespecifyapplets.htm
tech.root: Intl
ms.assetid: 788C7272-3BFF-4531-B66E-211585BF85E3
ms.date: 12/05/2018
ms.keywords: IImeSpecifyApplets, IImeSpecifyApplets interface [Internationalization for Windows Applications], IImeSpecifyApplets interface [Internationalization for Windows Applications],described, imepad/IImeSpecifyApplets, intl.iimespecifyapplets
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImeSpecifyApplets
 - imepad/IImeSpecifyApplets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImeSpecifyApplets
---

# IImeSpecifyApplets interface


## -description

The <b>IImeSpecifyApplets</b> interface specifies methods called from the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface object to emulate the <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImeSpecifyApplets</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImeSpecifyApplets</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImeSpecifyApplets</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imepad/nf-imepad-iimespecifyapplets-getappletiidlist">GetAppletIIDList</a>
</td>
<td align="left" width="63%">
Called from the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface to enumerate the <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> interfaces that are implemented.

</td>
</tr>
</table>