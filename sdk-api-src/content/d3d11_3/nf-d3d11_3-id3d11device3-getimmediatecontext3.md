---
UID: NF:d3d11_3.ID3D11Device3.GetImmediateContext3
title: ID3D11Device3::GetImmediateContext3 (d3d11_3.h)
description: Gets an immediate context, which can play back command lists. (ID3D11Device3.GetImmediateContext3)
helpviewer_keywords: ["GetImmediateContext3","GetImmediateContext3 method [Direct3D 11]","GetImmediateContext3 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","GetImmediateContext3 method","ID3D11Device3.GetImmediateContext3","ID3D11Device3::GetImmediateContext3","d3d11_3/ID3D11Device3::GetImmediateContext3","direct3d11.id3d11device3_getimmediatecontext3"]
old-location: direct3d11\id3d11device3_getimmediatecontext3.htm
tech.root: direct3d11
ms.assetid: E9E247C3-6326-46AC-A742-F5A4BE701B5B
ms.date: 12/05/2018
ms.keywords: GetImmediateContext3, GetImmediateContext3 method [Direct3D 11], GetImmediateContext3 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],GetImmediateContext3 method, ID3D11Device3.GetImmediateContext3, ID3D11Device3::GetImmediateContext3, d3d11_3/ID3D11Device3::GetImmediateContext3, direct3d11.id3d11device3_getimmediatecontext3
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device3::GetImmediateContext3
 - d3d11_3/ID3D11Device3::GetImmediateContext3
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
 - ID3D11Device3.GetImmediateContext3
---

# ID3D11Device3::GetImmediateContext3


## -description

Gets an immediate context, which can play back <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>.

## -parameters

### -param ppImmediateContext [out]

Type: <b><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a>**</b>

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a> interface pointer is initialized.

## -remarks

The
         <b>GetImmediateContext3</b> method outputs an
          <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a> object that represents an immediate context, which is used to perform rendering that you want immediately submitted to a device.
          For most apps, an immediate context is the primary object that is used to draw your scene.
        

The <b>GetImmediateContext3</b> method increments the reference count of the immediate context by one.
          Therefore, you must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-getimmediatecontext1">ID3D11Device1::GetImmediateContext1</a>



<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-getimmediatecontext2">ID3D11Device2::GetImmediateContext2</a>



<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext">ID3D11Device::GetImmediateContext</a>
