---
UID: NN:fhcfg.IFhTarget
title: IFhTarget (fhcfg.h)
description: The IFhTarget interface allows client applications to read numeric and string properties of a File History backup target.
helpviewer_keywords: ["IFhTarget","IFhTarget interface [Windows API]","IFhTarget interface [Windows API]","described","fhcfg/IFhTarget","winprog.ifhtarget"]
old-location: winprog\ifhtarget.htm
tech.root: winprog
ms.assetid: 5A73A81A-72A3-4794-86E5-9CA8FCA200C0
ms.date: 12/05/2018
ms.keywords: IFhTarget, IFhTarget interface [Windows API], IFhTarget interface [Windows API],described, fhcfg/IFhTarget, winprog.ifhtarget
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhTarget
 - fhcfg/IFhTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhTarget
---

# IFhTarget interface


## -description

The <b>IFhTarget</b> interface allows client applications to read numeric and string properties of a File History backup target.

> [!NOTE] 
> **IFhTarget** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFhTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getnumericalproperty">GetNumericalProperty</a>
</td>
<td align="left" width="63%">
Retrieves a numeric property of the File History backup target that is represented by an <b>IFhTarget</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getstringproperty">GetStringProperty</a>
</td>
<td align="left" width="63%">
Retrieves a string property of the File History backup target that is represented by an <b>IFhTarget</b> interface.

</td>
</tr>
</table>