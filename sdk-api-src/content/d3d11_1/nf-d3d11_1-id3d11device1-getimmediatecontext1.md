---
UID: NF:d3d11_1.ID3D11Device1.GetImmediateContext1
title: ID3D11Device1::GetImmediateContext1 (d3d11_1.h)
description: Gets an immediate context, which can play back command lists. (ID3D11Device1.GetImmediateContext1)
helpviewer_keywords: ["GetImmediateContext1","GetImmediateContext1 method [Direct3D 11]","GetImmediateContext1 method [Direct3D 11]","ID3D11Device1 interface","ID3D11Device1 interface [Direct3D 11]","GetImmediateContext1 method","ID3D11Device1.GetImmediateContext1","ID3D11Device1::GetImmediateContext1","d3d11_1/ID3D11Device1::GetImmediateContext1","direct3d11.id3d11device1_getimmediatecontext1"]
old-location: direct3d11\id3d11device1_getimmediatecontext1.htm
tech.root: direct3d11
ms.assetid: E66CDC7E-21B5-4675-A7A1-6F94940A4C13
ms.date: 12/05/2018
ms.keywords: GetImmediateContext1, GetImmediateContext1 method [Direct3D 11], GetImmediateContext1 method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],GetImmediateContext1 method, ID3D11Device1.GetImmediateContext1, ID3D11Device1::GetImmediateContext1, d3d11_1/ID3D11Device1::GetImmediateContext1, direct3d11.id3d11device1_getimmediatecontext1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11Device1::GetImmediateContext1
 - d3d11_1/ID3D11Device1::GetImmediateContext1
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
 - ID3D11Device1.GetImmediateContext1
---

# ID3D11Device1::GetImmediateContext1


## -description

Gets an immediate context, which can play back command lists.

## -parameters

### -param ppImmediateContext [out]

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a> interface pointer is initialized.

## -remarks

<b>GetImmediateContext1</b> returns an <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a> object that represents an immediate context. You can use this immediate context to perform rendering that you want immediately submitted to a device. For most applications, an immediate context is the primary object that is used to draw your scene.

<b>GetImmediateContext1</b> increments the reference count of the immediate context by one. So, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>
