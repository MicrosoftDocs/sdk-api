---
UID: NF:d3d9.IDirect3DDevice9.EndStateBlock
title: IDirect3DDevice9::EndStateBlock (d3d9.h)
description: Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.helpviewer_keywords: ["1893d4cf-9e96-8cbc-4c69-17f309bf0986","EndStateBlock","EndStateBlock method [Direct3D 9]","EndStateBlock method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","EndStateBlock method","IDirect3DDevice9.EndStateBlock","IDirect3DDevice9::EndStateBlock","d3d9helper/IDirect3DDevice9::EndStateBlock","direct3d9.idirect3ddevice9__endstateblock"]
old-location: direct3d9\idirect3ddevice9__endstateblock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__endstateblock.htm
ms.date: 12/05/2018
ms.keywords: 1893d4cf-9e96-8cbc-4c69-17f309bf0986, EndStateBlock, EndStateBlock method [Direct3D 9], EndStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EndStateBlock method, IDirect3DDevice9.EndStateBlock, IDirect3DDevice9::EndStateBlock, d3d9helper/IDirect3DDevice9::EndStateBlock, direct3d9.idirect3ddevice9__endstateblock
f1_keywords:
- d3d9/IDirect3DDevice9.EndStateBlock
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DDevice9.EndStateBlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::EndStateBlock


## -description


Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.


## -parameters




### -param ppSB [in, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dstateblock9">IDirect3DStateBlock9</a>**</b>

Pointer to a state block interface. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dstateblock9">IDirect3DStateBlock9</a>.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginstateblock">IDirect3DDevice9::BeginStateBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createstateblock">IDirect3DDevice9::CreateStateBlock</a>
 

 

