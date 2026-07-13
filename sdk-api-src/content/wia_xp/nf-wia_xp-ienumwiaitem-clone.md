---
UID: NF:wia_xp.IEnumWiaItem.Clone
title: IEnumWiaItem::Clone (wia_xp.h)
description: The IEnumWiaItem::Clone method creates an additional instance of the IEnumWiaItem interface and sends back a pointer to it.
helpviewer_keywords: ["Clone","Clone method [WIA]","Clone method [WIA]","IEnumWiaItem interface","IEnumWiaItem interface [WIA]","Clone method","IEnumWiaItem.Clone","IEnumWiaItem::Clone","_wia_IEnumWiaItem_Clone","wia._wia_IEnumWiaItem_Clone","wia_xp/IEnumWiaItem::Clone"]
old-location: wia\_wia_IEnumWiaItem_Clone.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwiaitem\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [WIA], Clone method [WIA],IEnumWiaItem interface, IEnumWiaItem interface [WIA],Clone method, IEnumWiaItem.Clone, IEnumWiaItem::Clone, _wia_IEnumWiaItem_Clone, wia._wia_IEnumWiaItem_Clone, wia_xp/IEnumWiaItem::Clone
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
 - IEnumWiaItem::Clone
 - wia_xp/IEnumWiaItem::Clone
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
 - IEnumWiaItem.Clone
archived: true
---

# IEnumWiaItem::Clone


## -description

The <b>IEnumWiaItem::Clone</b> method creates an additional instance of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem">IEnumWiaItem</a> interface and sends back a pointer to it.

## -parameters

### -param ppIEnum [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem">IEnumWiaItem</a>**</b>

Pointer  to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem">IEnumWiaItem</a> interface. Receives the address of the <b>IEnumWiaItem</b> interface instance that <b>IEnumWiaItem::Clone</b> creates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.