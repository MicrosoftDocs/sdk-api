---
UID: NF:d3d9helper.IDirect3D9.GetAdapterIdentifier
title: IDirect3D9::GetAdapterIdentifier (d3d9helper.h)
description: The IDirect3D9::GetAdapterIdentifier (d3d9helper.h) method describes the physical display adapters present in the system when the IDirect3D9 interface was instantiated.
helpviewer_keywords: ["GetAdapterIdentifier","GetAdapterIdentifier method [Direct3D 9]","GetAdapterIdentifier method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","GetAdapterIdentifier method","IDirect3D9.GetAdapterIdentifier","IDirect3D9::GetAdapterIdentifier","ab3a7dce-1e55-5674-03b7-13a53540bbf5","d3d9helper/IDirect3D9::GetAdapterIdentifier","direct3d9.idirect3d9__getadapteridentifier"]
old-location: direct3d9\idirect3d9__getadapteridentifier.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadapteridentifier.htm
ms.date: 08/11/2022
ms.keywords: GetAdapterIdentifier, GetAdapterIdentifier method [Direct3D 9], GetAdapterIdentifier method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterIdentifier method, IDirect3D9.GetAdapterIdentifier, IDirect3D9::GetAdapterIdentifier, ab3a7dce-1e55-5674-03b7-13a53540bbf5, d3d9helper/IDirect3D9::GetAdapterIdentifier, direct3d9.idirect3d9__getadapteridentifier
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
 - IDirect3D9::GetAdapterIdentifier
 - d3d9helper/IDirect3D9::GetAdapterIdentifier
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
 - IDirect3D9.GetAdapterIdentifier
---

# IDirect3D9::GetAdapterIdentifier


## -description

Describes the physical display adapters present in the system when the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> interface was instantiated.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. The minimum value for this parameter is 0, and the maximum value for this parameter is one less than the value returned by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadaptercount">GetAdapterCount</a>.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags sets the <b>WHQLLevel</b> member of <a href="/windows/desktop/direct3d9/d3dadapter-identifier9">D3DADAPTER_IDENTIFIER9</a>. Flags can be set to either 0 or D3DENUM_WHQL_LEVEL. If D3DENUM_WHQL_LEVEL is specified, this call can connect to the Internet to download new Microsoft Windows Hardware Quality Labs (WHQL) certificates.

Differences between Direct3D 9 and Direct3D 9Ex:

D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system). Any of these operating systems return 1 in the <b>WHQLLevel</b> member of <a href="/windows/desktop/direct3d9/d3dadapter-identifier9">D3DADAPTER_IDENTIFIER9</a> without checking the status of the driver.

### -param pIdentifier [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dadapter-identifier9">D3DADAPTER_IDENTIFIER9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dadapter-identifier9">D3DADAPTER_IDENTIFIER9</a> structure to be filled with information describing this adapter. If <i>Adapter</i> is greater than or equal to the number of adapters in the system, this structure will be zeroed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if Adapter is out of range, if Flags contains unrecognized parameters, or if pIdentifier is <b>NULL</b> or points to unwritable memory.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadaptercount">GetAdapterCount</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
