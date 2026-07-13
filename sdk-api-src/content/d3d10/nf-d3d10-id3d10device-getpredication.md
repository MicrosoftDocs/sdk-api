---
UID: NF:d3d10.ID3D10Device.GetPredication
title: ID3D10Device::GetPredication (d3d10.h)
description: Get the rendering predicate state. (ID3D10Device.GetPredication)
helpviewer_keywords: ["7e48b41e-557d-8a50-cf4b-b3309c77e0af","GetPredication","GetPredication method [Direct3D 10]","GetPredication method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GetPredication method","ID3D10Device.GetPredication","ID3D10Device::GetPredication","d3d10/ID3D10Device::GetPredication","direct3d10.id3d10device_getpredication"]
old-location: direct3d10\id3d10device_getpredication.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getpredication.htm
ms.date: 12/05/2018
ms.keywords: 7e48b41e-557d-8a50-cf4b-b3309c77e0af, GetPredication, GetPredication method [Direct3D 10], GetPredication method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetPredication method, ID3D10Device.GetPredication, ID3D10Device::GetPredication, d3d10/ID3D10Device::GetPredication, direct3d10.id3d10device_getpredication
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GetPredication
 - d3d10/ID3D10Device::GetPredication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GetPredication
---

# ID3D10Device::GetPredication


## -description

Get the rendering predicate state.

## -parameters

### -param ppPredicate [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate</a>). Value stored here will be <b>NULL</b> upon device creation.

### -param pPredicateValue [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Address of a boolean to fill with the predicate comparison value. <b>FALSE</b> upon device creation.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
