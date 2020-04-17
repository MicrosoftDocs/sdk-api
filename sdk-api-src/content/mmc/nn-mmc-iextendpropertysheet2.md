---
UID: NN:mmc.IExtendPropertySheet2
title: IExtendPropertySheet2 (mmc.h)
description: The IExtendPropertySheet2 interface is introduced in MMC 1.1.helpviewer_keywords: ["IExtendPropertySheet2","IExtendPropertySheet2 interface [MMC]","IExtendPropertySheet2 interface [MMC]","described","_slate_iextendpropertysheet2","mmc.iextendpropertysheet2","mmc/IExtendPropertySheet2"]
old-location: mmc\iextendpropertysheet2.htm
tech.root: mmc
ms.assetid: 9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d
ms.date: 12/05/2018
ms.keywords: IExtendPropertySheet2, IExtendPropertySheet2 interface [MMC], IExtendPropertySheet2 interface [MMC],described, _slate_iextendpropertysheet2, mmc.iextendpropertysheet2, mmc/IExtendPropertySheet2
f1_keywords:
- mmc/IExtendPropertySheet2
dev_langs:
- c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
- Mmc.h
api_name:
- IExtendPropertySheet2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendPropertySheet2 interface


## -description


The 
<b>IExtendPropertySheet2</b> interface is introduced in MMC 1.1.

The 
<b>IExtendPropertySheet2</b> interface enables a snap-in component to add pages to the property sheet of an item.

<b>IExtendPropertySheet2</b> supersedes the <b>IExtendPropertySheet</b> interface for MMC 1.1. In addition to inheriting all of the methods of <b>IExtendPropertySheet</b>, 
<b>IExtendPropertySheet2</b> has the following method:


<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendpropertysheet2-getwatermarks">IExtendPropertySheet2::GetWatermarks</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendPropertySheet2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendPropertySheet2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendPropertySheet2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">CreatePropertyPages</a>
</td>
<td align="left" width="63%">
Adds pages to a property sheet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendpropertysheet2-getwatermarks">GetWatermarks</a>
</td>
<td align="left" width="63%">
Gets the watermark and header bitmap for the Wizard 97 style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814849(v=vs.85)">QueryPagesFor</a>
</td>
<td align="left" width="63%">
Determines whether the object needs pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/adding-property-pages-and-wizard-pages">Adding Property Pages and Wizard Pages</a>
 

 

