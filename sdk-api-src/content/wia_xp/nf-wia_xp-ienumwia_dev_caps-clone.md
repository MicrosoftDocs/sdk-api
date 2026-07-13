---
UID: NF:wia_xp.IEnumWIA_DEV_CAPS.Clone
title: IEnumWIA_DEV_CAPS::Clone (wia_xp.h)
description: The IEnumWIA_DEV_CAPS::Clone method creates an additional instance of the IEnumWIA_DEV_CAPS interface and sends back a pointer to it.
helpviewer_keywords: ["Clone","Clone method [WIA]","Clone method [WIA]","IEnumWIA_DEV_CAPS interface","IEnumWIA_DEV_CAPS interface [WIA]","Clone method","IEnumWIA_DEV_CAPS.Clone","IEnumWIA_DEV_CAPS::Clone","_wia_IEnumWIA_DEV_CAPS_Clone","wia._wia_IEnumWIA_DEV_CAPS_Clone","wia_xp/IEnumWIA_DEV_CAPS::Clone"]
old-location: wia\_wia_IEnumWIA_DEV_CAPS_Clone.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwia_dev_caps\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [WIA], Clone method [WIA],IEnumWIA_DEV_CAPS interface, IEnumWIA_DEV_CAPS interface [WIA],Clone method, IEnumWIA_DEV_CAPS.Clone, IEnumWIA_DEV_CAPS::Clone, _wia_IEnumWIA_DEV_CAPS_Clone, wia._wia_IEnumWIA_DEV_CAPS_Clone, wia_xp/IEnumWIA_DEV_CAPS::Clone
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
 - IEnumWIA_DEV_CAPS::Clone
 - wia_xp/IEnumWIA_DEV_CAPS::Clone
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
 - IEnumWIA_DEV_CAPS.Clone
archived: true
---

# IEnumWIA_DEV_CAPS::Clone


## -description

The <b>IEnumWIA_DEV_CAPS::Clone</b> method creates an additional instance of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> interface and sends back a pointer to it.

## -parameters

### -param ppIEnum [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a>**</b>

Contains the address of a pointer to the instance of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> that <b>IEnumWIA_DEV_CAPS::Clone</b> creates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the pointers they receive through the <i>ppIEnum</i> parameter.