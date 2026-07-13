---
UID: NN:wia_xp.IEnumWiaItem
title: IEnumWiaItem (wia_xp.h)
description: The IEnumWiaItem interface is used by applications to enumerate IWiaItem objects in the tree's current folder.
helpviewer_keywords: ["IEnumWiaItem","IEnumWiaItem interface [WIA]","IEnumWiaItem interface [WIA]","described","_wia_IEnumWiaItem","wia._wia_IEnumWiaItem","wia_xp/IEnumWiaItem"]
old-location: wia\_wia_IEnumWiaItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\ienumwiaitem.htm
ms.date: 12/05/2018
ms.keywords: IEnumWiaItem, IEnumWiaItem interface [WIA], IEnumWiaItem interface [WIA],described, _wia_IEnumWiaItem, wia._wia_IEnumWiaItem, wia_xp/IEnumWiaItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWiaItem
 - wia_xp/IEnumWiaItem
dev_langs:
 - c++
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
archived: true
---

# IEnumWiaItem interface


## -description

The <b>IEnumWiaItem</b> interface is used by applications to enumerate <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects in the tree's current folder. The Windows Image Acquisition (WIA) run-time system represents every WIA hardware device to applications as a hierarchical tree of <b>IWiaItem</b> objects.

<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="/windows/desktop/wia/-wia-ienumwiaitem2">IEnumWiaItem2</a> instead of <b>IEnumWiaItem</b>.</div><div> </div>

## -inheritance

The <b>IEnumWiaItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWiaItem</b> also has these types of members:

## -remarks

The <b>IEnumWiaItem</b> interface is a specific implementation for WIA of the standard Component Object Model (COM) enumeration interface. For details, see <a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWiaItem</b> interface by invoking the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems">IWiaItem::EnumChildItems</a> method.

The <b>IEnumWiaItem</b> interface, like all COM interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems">EnumChildItems</a>



<a href="/windows/desktop/wia/-wia-enumerating-items">Enumerating Items</a>



<a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
