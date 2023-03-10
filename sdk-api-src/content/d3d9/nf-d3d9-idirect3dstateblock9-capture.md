---
UID: NF:d3d9.IDirect3DStateBlock9.Capture
title: IDirect3DStateBlock9::Capture (d3d9.h)
description: The IDirect3DStateBlock9::Capture (d3d9.h) method captures the current value of states that are included in a stateblock.
helpviewer_keywords: ["2f57837a-b161-c1f5-e5ba-7e4fda75185f","Capture","Capture method [Direct3D 9]","Capture method [Direct3D 9]","IDirect3DStateBlock9 interface","IDirect3DStateBlock9 interface [Direct3D 9]","Capture method","IDirect3DStateBlock9.Capture","IDirect3DStateBlock9::Capture","d3d9helper/IDirect3DStateBlock9::Capture","direct3d9.idirect3dstateblock9__capture"]
old-location: direct3d9\idirect3dstateblock9__capture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dstateblock9__capture.htm
ms.date: 08/11/2022
ms.keywords: 2f57837a-b161-c1f5-e5ba-7e4fda75185f, Capture, Capture method [Direct3D 9], Capture method [Direct3D 9],IDirect3DStateBlock9 interface, IDirect3DStateBlock9 interface [Direct3D 9],Capture method, IDirect3DStateBlock9.Capture, IDirect3DStateBlock9::Capture, d3d9helper/IDirect3DStateBlock9::Capture, direct3d9.idirect3dstateblock9__capture
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DStateBlock9::Capture
 - d3d9/IDirect3DStateBlock9::Capture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DStateBlock9.Capture
---

# IDirect3DStateBlock9::Capture


## -description

Capture the current value of states that are included in a stateblock.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails because capture cannot be done while in record mode, the return value is D3DERR_INVALIDCALL.

## -remarks

The Capture method captures current values for states within an existing state block. It does not capture the entire state of the device. For example:


```

IDirect3DStateBlock9* pStateBlock = NULL;

pd3dDevice->BeginStateBlock();
// Add the ZENABLE state to the stateblock 
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, D3DZB_TRUE );
pd3dDevice->EndStateBlock ( &pStateBlock );
    
// Change the current value that is stored in the state block
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, D3DZB_FALSE );
pStateBlock->Capture();			

pStateBlock->Release();

```


Creating an empty stateblock and calling the Capture method does nothing if no states have been set.

The Capture method  will not capture information for lights that are explicitly or implicitly created after the stateblock is created.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dstateblock9">IDirect3DStateBlock9</a>
