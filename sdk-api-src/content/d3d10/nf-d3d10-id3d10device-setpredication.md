---
UID: NF:d3d10.ID3D10Device.SetPredication
title: ID3D10Device::SetPredication (d3d10.h)
description: Set a rendering predicate. (ID3D10Device.SetPredication)
helpviewer_keywords: ["20a67636-3d02-6716-b38e-39b2f601230b","ID3D10Device interface [Direct3D 10]","SetPredication method","ID3D10Device.SetPredication","ID3D10Device::SetPredication","SetPredication","SetPredication method [Direct3D 10]","SetPredication method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::SetPredication","direct3d10.id3d10device_setpredication"]
old-location: direct3d10\id3d10device_setpredication.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setpredication.htm
ms.date: 12/05/2018
ms.keywords: 20a67636-3d02-6716-b38e-39b2f601230b, ID3D10Device interface [Direct3D 10],SetPredication method, ID3D10Device.SetPredication, ID3D10Device::SetPredication, SetPredication, SetPredication method [Direct3D 10], SetPredication method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetPredication, direct3d10.id3d10device_setpredication
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
 - ID3D10Device::SetPredication
 - d3d10/ID3D10Device::SetPredication
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
 - ID3D10Device.SetPredication
---

# ID3D10Device::SetPredication


## -description

Set a rendering predicate.

## -parameters

### -param pPredicate [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate</a>*</b>

Pointer to a predicate (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate</a>). A <b>NULL</b> value indicates "no" predication; in this case, the value of PredicateValue is irrelevant but will be preserved for <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getpredication">ID3D10Device::GetPredication</a>.

### -param PredicateValue [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.

## -remarks

The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a> are invalid.

This method is used to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting Predicate data of the Predicate is equal to the PredicateValue. However, some Predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of Predication is to allow an application to issue graphics commands without taking the performance hit of spinning, waiting for <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> to return. So, Predication can occur while <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. Another way to think of it: an application can also use Predication as a fallback, if it is possible that <b>ID3D10Asynchronous::GetData</b> returns S_FALSE. If <b>ID3D10Asynchronous::GetData</b> returns S_OK, the application can skip calling the graphics commands manually with its own application logic.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
