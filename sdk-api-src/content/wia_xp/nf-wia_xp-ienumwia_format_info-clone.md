---
UID: NF:wia_xp.IEnumWIA_FORMAT_INFO.Clone
title: IEnumWIA_FORMAT_INFO::Clone (wia_xp.h)
description: The IEnumWIA_FORMAT_INFO::Clone method creates an additional instance of the IEnumWIA_FORMAT_INFO interface and returns an interface pointer to the new interface.
helpviewer_keywords: ["Clone","Clone method [WIA]","Clone method [WIA]","IEnumWIA_FORMAT_INFO interface","IEnumWIA_FORMAT_INFO interface [WIA]","Clone method","IEnumWIA_FORMAT_INFO.Clone","IEnumWIA_FORMAT_INFO::Clone","_wia_IEnumWIA_FORMAT_INFO_Clone","wia._wia_IEnumWIA_FORMAT_INFO_Clone","wia_xp/IEnumWIA_FORMAT_INFO::Clone"]
old-location: wia\_wia_IEnumWIA_FORMAT_INFO_Clone.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwia_format_info\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [WIA], Clone method [WIA],IEnumWIA_FORMAT_INFO interface, IEnumWIA_FORMAT_INFO interface [WIA],Clone method, IEnumWIA_FORMAT_INFO.Clone, IEnumWIA_FORMAT_INFO::Clone, _wia_IEnumWIA_FORMAT_INFO_Clone, wia._wia_IEnumWIA_FORMAT_INFO_Clone, wia_xp/IEnumWIA_FORMAT_INFO::Clone
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
 - IEnumWIA_FORMAT_INFO::Clone
 - wia_xp/IEnumWIA_FORMAT_INFO::Clone
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
 - IEnumWIA_FORMAT_INFO.Clone
archived: true
---

# IEnumWIA_FORMAT_INFO::Clone


## -description

The <b>IEnumWIA_FORMAT_INFO::Clone</b> method creates an additional instance of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info">IEnumWIA_FORMAT_INFO</a> interface and returns an interface pointer to the new interface.

## -parameters

### -param ppIEnum [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info">IEnumWIA_FORMAT_INFO</a>**</b>

Pointer to a new <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info">IEnumWIA_FORMAT_INFO</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.