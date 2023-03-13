---
UID: NF:d3d10.ID3D10Device.IAGetInputLayout
title: ID3D10Device::IAGetInputLayout (d3d10.h)
description: Get a pointer to the input-layout object that is bound to the input-assembler stage. (ID3D10Device.IAGetInputLayout)
helpviewer_keywords: ["IAGetInputLayout","IAGetInputLayout method [Direct3D 10]","IAGetInputLayout method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","IAGetInputLayout method","ID3D10Device.IAGetInputLayout","ID3D10Device::IAGetInputLayout","d3d10/ID3D10Device::IAGetInputLayout","direct3d10.id3d10device_iagetinputlayout","fc7e34a5-1fc3-6283-98db-681a4f1138cf"]
old-location: direct3d10\id3d10device_iagetinputlayout.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetinputlayout.htm
ms.date: 12/05/2018
ms.keywords: IAGetInputLayout, IAGetInputLayout method [Direct3D 10], IAGetInputLayout method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IAGetInputLayout method, ID3D10Device.IAGetInputLayout, ID3D10Device::IAGetInputLayout, d3d10/ID3D10Device::IAGetInputLayout, direct3d10.id3d10device_iagetinputlayout, fc7e34a5-1fc3-6283-98db-681a4f1138cf
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::IAGetInputLayout
 - d3d10/ID3D10Device::IAGetInputLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.h
api_name:
 - ID3D10Device.IAGetInputLayout
---

# ID3D10Device::IAGetInputLayout


## -description

Get a pointer to the input-layout object that is bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

## -parameters

### -param ppInputLayout [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10inputlayout">ID3D10InputLayout</a>**</b>

A pointer to the input-layout object (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10inputlayout">ID3D10InputLayout</a>), which describes the input buffers that will be read by the IA stage.

## -remarks

For information about creating an input-layout object, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">Creating the Input-Layout Object</a>.

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
