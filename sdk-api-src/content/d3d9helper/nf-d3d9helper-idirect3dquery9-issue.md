---
UID: NF:d3d9helper.IDirect3DQuery9.Issue
title: IDirect3DQuery9::Issue (d3d9helper.h)
description: The IDirect3DQuery9::Issue method (d3d9helper.h) issues a query.
helpviewer_keywords: ["7cfc335e-94a2-b744-65d5-5e6014ce4ff5","IDirect3DQuery9 interface [Direct3D 9]","Issue method","IDirect3DQuery9.Issue","IDirect3DQuery9::Issue","Issue","Issue method [Direct3D 9]","Issue method [Direct3D 9]","IDirect3DQuery9 interface","d3d9helper/IDirect3DQuery9::Issue","direct3d9.idirect3dquery9__issue"]
old-location: direct3d9\idirect3dquery9__issue.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9__issue.htm
ms.date: 08/11/2022
ms.keywords: 7cfc335e-94a2-b744-65d5-5e6014ce4ff5, IDirect3DQuery9 interface [Direct3D 9],Issue method, IDirect3DQuery9.Issue, IDirect3DQuery9::Issue, Issue, Issue method [Direct3D 9], Issue method [Direct3D 9],IDirect3DQuery9 interface, d3d9helper/IDirect3DQuery9::Issue, direct3d9.idirect3dquery9__issue
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
 - IDirect3DQuery9::Issue
 - d3d9helper/IDirect3DQuery9::Issue
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
 - IDirect3DQuery9.Issue
---

# IDirect3DQuery9::Issue


## -description

Issue a query.

## -parameters

### -param dwIssueFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Query flags specify the type of state change for the query. See <a href="/windows/desktop/direct3d9/d3dissue-begin">D3DISSUE_BEGIN</a> and <a href="/windows/desktop/direct3d9/d3dissue-end">D3DISSUE_END</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

A signaled query means the query has completed, the data is available, and <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata">IDirect3DQuery9::GetData</a> will return S_OK.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9">IDirect3DQuery9</a>
