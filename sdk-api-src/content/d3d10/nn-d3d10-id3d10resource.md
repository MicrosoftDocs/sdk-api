---
UID: NN:d3d10.ID3D10Resource
title: ID3D10Resource (d3d10.h)
description: A resource interface provides common actions on all resources. (ID3D10Resource)
helpviewer_keywords: ["ID3D10Resource","ID3D10Resource interface [Direct3D 10]","ID3D10Resource interface [Direct3D 10]","described","a827797e-b4b8-c82b-c567-463061c6d963","d3d10/ID3D10Resource","direct3d10.id3d10resource"]
old-location: direct3d10\id3d10resource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Resource, ID3D10Resource interface [Direct3D 10], ID3D10Resource interface [Direct3D 10],described, a827797e-b4b8-c82b-c567-463061c6d963, d3d10/ID3D10Resource, direct3d10.id3d10resource
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Resource
 - d3d10/ID3D10Resource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Resource
---

# ID3D10Resource interface


## -description

A resource interface provides common actions on all <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resources</a>.

## -inheritance

The <b>ID3D10Resource</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10Resource</b> also has these types of members:

## -remarks

A resource interface cannot be created directly; instead, <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffers</a> and textures are created that inherit from a resource interface (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Creating Buffer Resources</a> or <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating-textures">Creating Texture Resources</a>).

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
