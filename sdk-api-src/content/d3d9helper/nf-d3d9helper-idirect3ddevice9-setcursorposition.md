---
UID: NF:d3d9helper.IDirect3DDevice9.SetCursorPosition
title: IDirect3DDevice9::SetCursorPosition (d3d9helper.h)
description: The IDirect3DDevice9::SetCursorPosition method (d3d9.h) sets the cursor position and update options. 
helpviewer_keywords: ["40c9d24c-baf1-aaaf-5f7b-a462b05b36b5","D3DCURSOR_IMMEDIATE_UPDATE","IDirect3DDevice9 interface [Direct3D 9]","SetCursorPosition method","IDirect3DDevice9.SetCursorPosition","IDirect3DDevice9::SetCursorPosition","SetCursorPosition","SetCursorPosition method [Direct3D 9]","SetCursorPosition method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetCursorPosition","direct3d9.idirect3ddevice9__setcursorposition"]
old-location: direct3d9\idirect3ddevice9__setcursorposition.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setcursorposition.htm
ms.date: 08/11/2022
ms.keywords: 40c9d24c-baf1-aaaf-5f7b-a462b05b36b5, D3DCURSOR_IMMEDIATE_UPDATE, IDirect3DDevice9 interface [Direct3D 9],SetCursorPosition method, IDirect3DDevice9.SetCursorPosition, IDirect3DDevice9::SetCursorPosition, SetCursorPosition, SetCursorPosition method [Direct3D 9], SetCursorPosition method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetCursorPosition, direct3d9.idirect3ddevice9__setcursorposition
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
 - IDirect3DDevice9::SetCursorPosition
 - d3d9helper/IDirect3DDevice9::SetCursorPosition
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
 - IDirect3DDevice9.SetCursorPosition
---

# IDirect3DDevice9::SetCursorPosition


## -description

Sets the cursor position and update options.

## -parameters

### -param X [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The new X-position of the cursor in virtual desktop coordinates. See Remarks.

### -param Y [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The new Y-position of the cursor in virtual desktop coordinates. See Remarks.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


Specifies the update options for the cursor. Currently, only one flag is defined.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DCURSOR_IMMEDIATE_UPDATE"></a><a id="d3dcursor_immediate_update"></a><dl>
<dt><b>D3DCURSOR_IMMEDIATE_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Update cursor at the refresh rate.

If this flag is specified, the system guarantees that the cursor will be updated at a minimum of half the display refresh rate, but never more frequently than the display refresh rate. Otherwise, the method delays cursor updates until the next <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> call. Not setting this flag usually results in better performance than if the flag is set. However, applications should set this flag if the rate of calls to Present is low enough that users would notice a significant delay in cursor motion. This flag has no effect in a windowed-mode application. Some video cards implement hardware color cursors. This flag does not have an effect on these cards.

</td>
</tr>
</table>

## -remarks

When running in full-screen mode, screen space coordinates are the back buffer coordinates appropriately scaled to the current display mode. When running in windowed mode, screen space coordinates are the desktop coordinates. The cursor image is drawn at the specified position minus the hotspot-offset specified by the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcursorproperties">SetCursorProperties</a> method.

If the cursor has been hidden by <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor">ShowCursor</a>, the cursor is not drawn.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcursorproperties">SetCursorProperties</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor">ShowCursor</a>
