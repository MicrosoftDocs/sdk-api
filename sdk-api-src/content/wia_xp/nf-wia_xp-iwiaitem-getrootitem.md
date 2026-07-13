---
UID: NF:wia_xp.IWiaItem.GetRootItem
title: IWiaItem::GetRootItem (wia_xp.h)
description: The IWiaItem::GetRootItem method retrieves the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) hardware device.
helpviewer_keywords: ["GetRootItem","GetRootItem method [WIA]","GetRootItem method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","GetRootItem method","IWiaItem.GetRootItem","IWiaItem::GetRootItem","_wia_IWiaItem_GetRootItem","wia._wia_IWiaItem_GetRootItem","wia_xp/IWiaItem::GetRootItem"]
old-location: wia\_wia_IWiaItem_GetRootItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\getrootitem.htm
ms.date: 12/05/2018
ms.keywords: GetRootItem, GetRootItem method [WIA], GetRootItem method [WIA],IWiaItem interface, IWiaItem interface [WIA],GetRootItem method, IWiaItem.GetRootItem, IWiaItem::GetRootItem, _wia_IWiaItem_GetRootItem, wia._wia_IWiaItem_GetRootItem, wia_xp/IWiaItem::GetRootItem
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
 - IWiaItem::GetRootItem
 - wia_xp/IWiaItem::GetRootItem
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
 - IWiaItem.GetRootItem
archived: true
---

# IWiaItem::GetRootItem


## -description

The <b>IWiaItem::GetRootItem</b> method retrieves the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) hardware device.

## -parameters

### -param ppIWiaItem [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> interface that contains a pointer to the <b>IWiaItem</b> interface of the root item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Given any <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object in the object tree of a WIA hardware device, the application retrieves a pointer to the root item by calling this function. 

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIWiaItem</i> parameter.