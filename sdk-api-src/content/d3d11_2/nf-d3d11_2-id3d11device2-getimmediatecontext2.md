---
UID: NF:d3d11_2.ID3D11Device2.GetImmediateContext2
title: ID3D11Device2::GetImmediateContext2 (d3d11_2.h)
description: Gets an immediate context, which can play back command lists. (ID3D11Device2.GetImmediateContext2)
helpviewer_keywords: ["GetImmediateContext2","GetImmediateContext2 method [Direct3D 11]","GetImmediateContext2 method [Direct3D 11]","ID3D11Device2 interface","ID3D11Device2 interface [Direct3D 11]","GetImmediateContext2 method","ID3D11Device2.GetImmediateContext2","ID3D11Device2::GetImmediateContext2","d3d11_2/ID3D11Device2::GetImmediateContext2","direct3d11.id3d11device2_getimmediatecontext2"]
old-location: direct3d11\id3d11device2_getimmediatecontext2.htm
tech.root: direct3d11
ms.assetid: 3DCA642D-7992-4C1E-8AD2-CA0099188A46
ms.date: 12/05/2018
ms.keywords: GetImmediateContext2, GetImmediateContext2 method [Direct3D 11], GetImmediateContext2 method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],GetImmediateContext2 method, ID3D11Device2.GetImmediateContext2, ID3D11Device2::GetImmediateContext2, d3d11_2/ID3D11Device2::GetImmediateContext2, direct3d11.id3d11device2_getimmediatecontext2
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device2::GetImmediateContext2
 - d3d11_2/ID3D11Device2::GetImmediateContext2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device2.GetImmediateContext2
---

# ID3D11Device2::GetImmediateContext2


## -description

Gets an immediate context, which can play back <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>.

## -parameters

### -param ppImmediateContext [out]

Type: <b><a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>**</b>

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a> interface pointer is initialized.

## -remarks

The <b>GetImmediateContext2</b> method returns an <a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a> object that represents an immediate context, which is used to perform rendering that you want immediately submitted to a device. For most apps, an immediate context is the primary object that is used to draw your scene.

The <b>GetImmediateContext2</b> method increments the reference count of the immediate context by one. Therefore, you must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2">ID3D11Device2</a>
