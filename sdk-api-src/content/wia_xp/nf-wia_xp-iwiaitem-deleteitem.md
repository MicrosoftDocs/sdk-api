---
UID: NF:wia_xp.IWiaItem.DeleteItem
title: IWiaItem::DeleteItem (wia_xp.h)
description: The IWiaItem::DeleteItem method removes the current IWiaItem object from the object tree of the device.
helpviewer_keywords: ["DeleteItem","DeleteItem method [WIA]","DeleteItem method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","DeleteItem method","IWiaItem.DeleteItem","IWiaItem::DeleteItem","_wia_IWiaItem_DeleteItem","wia._wia_IWiaItem_DeleteItem","wia_xp/IWiaItem::DeleteItem"]
old-location: wia\_wia_IWiaItem_DeleteItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\deleteitem.htm
ms.date: 12/05/2018
ms.keywords: DeleteItem, DeleteItem method [WIA], DeleteItem method [WIA],IWiaItem interface, IWiaItem interface [WIA],DeleteItem method, IWiaItem.DeleteItem, IWiaItem::DeleteItem, _wia_IWiaItem_DeleteItem, wia._wia_IWiaItem_DeleteItem, wia_xp/IWiaItem::DeleteItem
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
 - IWiaItem::DeleteItem
 - wia_xp/IWiaItem::DeleteItem
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
 - IWiaItem.DeleteItem
archived: true
---

# IWiaItem::DeleteItem


## -description

The <b>IWiaItem::DeleteItem</b> method removes the current <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object from the object tree of the device.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.

## -returns

Type: <b>HRESULT</b>

This method returns S_OK regardless of how many items were deleted. If the method fails, it returns a standard COM error code.

## -remarks

The Windows Image Acquisition (WIA) run-time system represents each WIA hardware device connected to the user's computer as a hierarchical tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects. A given WIA device may or may not allow applications to delete <b>IWiaItem</b> objects from its tree. Use the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> interface to query the device for item deletion capability.

If the device supports item deletion in its <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> tree, invoke the <b>IWiaItem::DeleteItem</b> method to remove the <b>IWiaItem</b> object. Note that this method will only delete an object after all references to the object have been released.