---
UID: NF:wia_xp.IEnumWiaItem.Skip
title: IEnumWiaItem::Skip (wia_xp.h)
description: The IEnumWiaItem::Skip method skips the specified number of items during an enumeration of available IWiaItem objects.
helpviewer_keywords: ["IEnumWiaItem interface [WIA]","Skip method","IEnumWiaItem.Skip","IEnumWiaItem::Skip","Skip","Skip method [WIA]","Skip method [WIA]","IEnumWiaItem interface","_wia_IEnumWiaItem_Skip","wia._wia_IEnumWiaItem_Skip","wia_xp/IEnumWiaItem::Skip"]
old-location: wia\_wia_IEnumWiaItem_Skip.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\skip.htm
ms.date: 12/05/2018
ms.keywords: IEnumWiaItem interface [WIA],Skip method, IEnumWiaItem.Skip, IEnumWiaItem::Skip, Skip, Skip method [WIA], Skip method [WIA],IEnumWiaItem interface, _wia_IEnumWiaItem_Skip, wia._wia_IEnumWiaItem_Skip, wia_xp/IEnumWiaItem::Skip
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
 - IEnumWiaItem::Skip
 - wia_xp/IEnumWiaItem::Skip
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
 - IEnumWiaItem.Skip
archived: true
---

# IEnumWiaItem::Skip


## -description

The <b>IEnumWiaItem::Skip</b> method skips the specified number of items during an enumeration of available <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of items to skip.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. If it is unable to skip the specified number of items, it returns S_FALSE. If the method fails, it returns a standard COM error code.