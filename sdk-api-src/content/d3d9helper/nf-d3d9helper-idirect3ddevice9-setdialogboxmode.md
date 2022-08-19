---
UID: NF:d3d9helper.IDirect3DDevice9.SetDialogBoxMode
title: IDirect3DDevice9::SetDialogBoxMode (d3d9helper.h)
description: The IDirect3DDevice9::SetDialogBoxMode method (d3d9.h) allows the use of GDI dialog boxes in full-screen mode applications.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetDialogBoxMode method","IDirect3DDevice9.SetDialogBoxMode","IDirect3DDevice9::SetDialogBoxMode","SetDialogBoxMode","SetDialogBoxMode method [Direct3D 9]","SetDialogBoxMode method [Direct3D 9]","IDirect3DDevice9 interface","a69d309f-e5c7-493a-e434-7700251e99ec","d3d9helper/IDirect3DDevice9::SetDialogBoxMode","direct3d9.idirect3ddevice9__setdialogboxmode"]
old-location: direct3d9\idirect3ddevice9__setdialogboxmode.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setdialogboxmode.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetDialogBoxMode method, IDirect3DDevice9.SetDialogBoxMode, IDirect3DDevice9::SetDialogBoxMode, SetDialogBoxMode, SetDialogBoxMode method [Direct3D 9], SetDialogBoxMode method [Direct3D 9],IDirect3DDevice9 interface, a69d309f-e5c7-493a-e434-7700251e99ec, d3d9helper/IDirect3DDevice9::SetDialogBoxMode, direct3d9.idirect3ddevice9__setdialogboxmode
req.header: d3d9helper.h
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
 - IDirect3DDevice9::SetDialogBoxMode
 - d3d9helper/IDirect3DDevice9::SetDialogBoxMode
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
 - IDirect3DDevice9.SetDialogBoxMode
---

# IDirect3DDevice9::SetDialogBoxMode


## -description

This method allows the use of GDI dialog boxes in full-screen mode applications.

## -parameters

### -param bEnableDialogs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to enable GDI dialog boxes, and <b>FALSE</b> to disable them.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL unless all of the following are true.



<ul>
<li>The application specified a back buffer format compatible with GDI, in other words, one of D3DFMT_X1R5G5B5, D3DFMT_R5G6B5, or D3DFMT_X8R8G8B8.</li>
<li>The application specified no multisampling.</li>
<li>The application specified D3DSWAPEFFECT_DISCARD.</li>
<li>The application specified D3DPRESENTFLAG_LOCKABLE_BACKBUFFER.</li>
<li>The application did not specify D3DCREATE_ADAPTERGROUP_DEVICE.</li>
<li>The application is not between BeginScene and EndScene.</li>
</ul>

## -remarks

The GDI dialog boxes must be created as child to the device window. They should also be created within the same thread that created the device because this enables the parent window to manage redrawing the child window.

The method has no effect for windowed mode applications, but this setting will be respected if the application resets the device into full-screen mode. If SetDialogBoxMode succeeds in a windowed mode application, any subsequent reset to full-screen mode will be checked against the restrictions listed above.  Also, SetDialogBoxMode causes all back buffers on the swap chain to be discarded, so an application is expected to refresh its content for all back buffers after this call.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
