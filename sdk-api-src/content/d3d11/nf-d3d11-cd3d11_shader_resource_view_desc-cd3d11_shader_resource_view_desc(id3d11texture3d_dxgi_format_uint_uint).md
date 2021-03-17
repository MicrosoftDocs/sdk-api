---
UID: NF:d3d11.CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D,DXGI_FORMAT,UINT,UINT)
title: CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D,DXGI_FORMAT,UINT,UINT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_SHADER_RESOURCE_VIEW_DESC structure that is initialized with 3D texture  values.
helpviewer_keywords: ["CD3D11_SHADER_RESOURCE_VIEW_DESC","CD3D11_SHADER_RESOURCE_VIEW_DESC interface [Direct3D 11]","CD3D11_SHADER_RESOURCE_VIEW_DESC method","CD3D11_SHADER_RESOURCE_VIEW_DESC method [Direct3D 11]","CD3D11_SHADER_RESOURCE_VIEW_DESC method [Direct3D 11]","CD3D11_SHADER_RESOURCE_VIEW_DESC interface","CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC","CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D","DXGI_FORMAT","UINT","UINT)","CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC","CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D","DXGI_FORMAT","UINT","UINT)","CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(const D3D11_SHADER_RESOURCE_VIEW_DESC&)","d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC","direct3d11.cd3d11_shader_resource_view_desc_cd3d11_shader_resource_view_desc_d3d11_shader_resource_view_desc_"]
old-location: 
tech.root: direct3d11
ms.assetid: D4D60701-ADB2-42E9-AA6F-3677221B6CE7
ms.date: 05/06/2019
ms.keywords: CD3D11_SHADER_RESOURCE_VIEW_DESC, CD3D11_SHADER_RESOURCE_VIEW_DESC interface [Direct3D 11],CD3D11_SHADER_RESOURCE_VIEW_DESC method, CD3D11_SHADER_RESOURCE_VIEW_DESC method [Direct3D 11], CD3D11_SHADER_RESOURCE_VIEW_DESC method [Direct3D 11],CD3D11_SHADER_RESOURCE_VIEW_DESC interface, CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC, CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D,DXGI_FORMAT,UINT,UINT), CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC, CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D,DXGI_FORMAT,UINT,UINT), CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(const D3D11_SHADER_RESOURCE_VIEW_DESC&), d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC, direct3d11.cd3d11_shader_resource_view_desc_cd3d11_shader_resource_view_desc_d3d11_shader_resource_view_desc_
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC
 - d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC
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
 - CD3D11_SHADER_RESOURCE_VIEW_DESC.CD3D11_SHADER_RESOURCE_VIEW_DESC
---

# CD3D11_SHADER_RESOURCE_VIEW_DESC::CD3D11_SHADER_RESOURCE_VIEW_DESC(ID3D11Texture3D,DXGI_FORMAT,UINT,UINT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151684(v=vs.85)">CD3D11_SHADER_RESOURCE_VIEW_DESC</a> structure that is initialized with 3D texture  values.

## -parameters

### -param pTex3D

A pointer to a **ID3D11Texture3D** interface for a 3D texture.

### -param format

A **DXGI_FORMAT**-typed value that specifies the viewing format.

### -param mostDetailedMip

Index of the most detailed mipmap level to use; this number is from 0 to *mipLevels* -1.

### -param mipLevels

The maximum number of mipmap levels for the view.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151684(v=vs.85)">CD3D11_SHADER_RESOURCE_VIEW_DESC</a>