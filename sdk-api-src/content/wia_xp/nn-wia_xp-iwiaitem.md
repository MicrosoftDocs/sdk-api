---
UID: NN:wia_xp.IWiaItem
title: IWiaItem (wia_xp.h)
description: Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of IWiaItem objects.
helpviewer_keywords: ["IWiaItem","IWiaItem interface [WIA]","IWiaItem interface [WIA]","described","_wia_IWiaItem","wia._wia_IWiaItem","wia_xp/IWiaItem"]
old-location: wia\_wia_IWiaItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\iwiaitem.htm
ms.date: 12/05/2018
ms.keywords: IWiaItem, IWiaItem interface [WIA], IWiaItem interface [WIA],described, _wia_IWiaItem, wia._wia_IWiaItem, wia_xp/IWiaItem
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
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaItem
 - wia_xp/IWiaItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem
archived: true
---

# IWiaItem interface


## -description

Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of <b>IWiaItem</b> objects. The <b>IWiaItem</b> interface provides applications with the ability to query devices to discover their capabilities. It also provides access to data transfer interfaces and item properties. In addition, the <b>IWiaItem</b> interface provides methods to enable applications to control the device.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="/windows/desktop/wia/-wia-iwiaitem2">IWiaItem2</a> instead of <b>IWiaItem</b>.</div><div> </div>

## -inheritance

The <b>IWiaItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaItem</b> also has these types of members:

## -remarks

Some of the methods of the <b>IWiaItem</b> interface are valid only on the root item of the device's tree. Other methods are valid on all items. The methods are grouped as follows:

<table class="clsStd">
<tr>
<td>Valid On Root Item Only</td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicecommand">IWiaItem::DeviceCommand</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg">IWiaItem::DeviceDlg</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities">IWiaItem::EnumDeviceCapabilities</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo">IWiaItem::EnumRegisterEventInfo</a>
</td>
</tr>
<tr>
<td>Valid On All Items</td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem">IWiaItem::AnalyzeItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-createchilditem">IWiaItem::CreateChildItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-deleteitem">IWiaItem::DeleteItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems">IWiaItem::EnumChildItems</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-finditembyname">IWiaItem::FindItemByName</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-getitemtype">IWiaItem::GetItemType</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-getrootitem">IWiaItem::GetRootItem</a>
</td>
</tr>
</table>
 

The <b>IWiaItem</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

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
