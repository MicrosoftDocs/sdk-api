---
UID: NN:strmif.IAMPhysicalPinInfo
title: IAMPhysicalPinInfo (strmif.h)
description: Note  This interface has been deprecated.
helpviewer_keywords: ["IAMPhysicalPinInfo","IAMPhysicalPinInfo interface [DirectShow]","IAMPhysicalPinInfo interface [DirectShow]","described","IAMPhysicalPinInfoInterface","dshow.iamphysicalpininfo","strmif/IAMPhysicalPinInfo"]
old-location: dshow\iamphysicalpininfo.htm
tech.root: dshow
ms.assetid: d1d05d2c-018e-421f-bfb9-810d708f726c
ms.date: 12/05/2018
ms.keywords: IAMPhysicalPinInfo, IAMPhysicalPinInfo interface [DirectShow], IAMPhysicalPinInfo interface [DirectShow],described, IAMPhysicalPinInfoInterface, dshow.iamphysicalpininfo, strmif/IAMPhysicalPinInfo
req.header: strmif.h
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
 - IAMPhysicalPinInfo
 - strmif/IAMPhysicalPinInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMPhysicalPinInfo
---

# IAMPhysicalPinInfo interface


## -description

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications and filters should not use it.</div>
<div> </div>
This interface enables an application or filter to retrieve information about a pin that represents a physical hardware connections.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMPhysicalPinInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMPhysicalPinInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMPhysicalPinInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamphysicalpininfo-getphysicaltype">GetPhysicalType</a>
</td>
<td align="left" width="63%">
Retrieves the type and name of the physical pin.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>

