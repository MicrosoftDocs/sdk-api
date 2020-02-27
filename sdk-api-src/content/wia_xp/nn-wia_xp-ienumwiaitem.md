---
UID: NN:wia_xp.IEnumWiaItem
title: IEnumWiaItem (wia_xp.h)
description: The IEnumWiaItem interface is used by applications to enumerate IWiaItem objects in the tree's current folder.
old-location: wia\_wia_IEnumWiaItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\ienumwiaitem.htm
ms.date: 12/05/2018
ms.keywords: IEnumWiaItem, IEnumWiaItem interface [WIA], IEnumWiaItem interface [WIA],described, _wia_IEnumWiaItem, wia._wia_IEnumWiaItem, wia_xp/IEnumWiaItem
f1_keywords:
- wia_xp/IEnumWiaItem
dev_langs:
- c++
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
api_name:
- IEnumWiaItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumWiaItem interface


## -description


The <b>IEnumWiaItem</b> interface is used by applications to enumerate <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects in the tree's current folder. The Windows Image Acquisition (WIA) run-time system represents every WIA hardware device to applications as a hierarchical tree of <b>IWiaItem</b> objects.

<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://docs.microsoft.com/windows/desktop/wia/-wia-ienumwiaitem2">IEnumWiaItem2</a> instead of <b>IEnumWiaItem</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWiaItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWiaItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWiaItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-clone">IEnumWiaItem::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-clone">IEnumWiaItem::Clone</a> method creates an additional instance of the <b>IEnumWiaItem</b> interface and sends back a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-getcount">IEnumWiaItem::GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-getcount">IEnumWiaItem::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-next">IEnumWiaItem::Next</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-next">IEnumWiaItem::Next</a> method fills an array of pointers to <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-reset">IEnumWiaItem::Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-reset">IEnumWiaItem::Reset</a> method is used by applications to restart the enumeration of item information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-skip">IEnumWiaItem::Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwiaitem-skip">IEnumWiaItem::Skip</a> method skips the specified number of items during an enumeration of available <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWiaItem</b> interface is a specific implementation for WIA of the standard Component Object Model (COM) enumeration interface. For details, see <a href="https://docs.microsoft.com/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWiaItem</b> interface by invoking the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems">IWiaItem::EnumChildItems</a> method.

The <b>IEnumWiaItem</b> interface, like all COM interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems">EnumChildItems</a>



<a href="https://docs.microsoft.com/windows/desktop/wia/-wia-enumerating-items">Enumerating Items</a>



<a href="https://docs.microsoft.com/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

