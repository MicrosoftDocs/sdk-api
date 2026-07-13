---
UID: NF:wia_xp.IWiaItem.GetItemType
title: IWiaItem::GetItemType (wia_xp.h)
description: The IWiaItem::GetItemType method is called by applications to obtain the type information of an item.
helpviewer_keywords: ["GetItemType","GetItemType method [WIA]","GetItemType method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","GetItemType method","IWiaItem.GetItemType","IWiaItem::GetItemType","_wia_IWiaItem_GetItemType","wia._wia_IWiaItem_GetItemType","wia_xp/IWiaItem::GetItemType"]
old-location: wia\_wia_IWiaItem_GetItemType.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\getitemtype.htm
ms.date: 12/05/2018
ms.keywords: GetItemType, GetItemType method [WIA], GetItemType method [WIA],IWiaItem interface, IWiaItem interface [WIA],GetItemType method, IWiaItem.GetItemType, IWiaItem::GetItemType, _wia_IWiaItem_GetItemType, wia._wia_IWiaItem_GetItemType, wia_xp/IWiaItem::GetItemType
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
 - IWiaItem::GetItemType
 - wia_xp/IWiaItem::GetItemType
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
 - IWiaItem.GetItemType
archived: true
---

# IWiaItem::GetItemType


## -description

The <b>IWiaItem::GetItemType</b> method is called by applications to obtain the type information of an item.

## -parameters

### -param pItemType [out]

Type: <b>LONG*</b>

Receives the address of a <b>LONG</b> variable that contains a combination of <a href="/windows/desktop/wia/-wia-wia-item-type-flags">WIA Item Type Flags</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Every <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) hardware device has a specific data type. Item objects represent folders and files. Folders contain file objects. File objects contain data acquired by the device such as images and sounds. This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.

An item may have more than one type. For example, an item that represents an audio file will have the type attributes <a href="/windows/desktop/wia/-wia-wia-item-type-flags">WiaItemTypeAudio</a> | <b>WiaItemTypeFile</b>.