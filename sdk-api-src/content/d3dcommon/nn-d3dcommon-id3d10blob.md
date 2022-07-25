---
UID: NN:d3dcommon.ID3D10Blob
title: ID3D10Blob (d3dcommon.h)
description: This interface is used to return arbitrary-length data.
helpviewer_keywords: ["ID3D10Blob","ID3D10Blob interface [Direct3D 11]","ID3D10Blob interface [Direct3D 11]","described","d3dcommon/ID3D10Blob","direct3d11.id3d10blob"]
old-location: direct3d11\id3d10blob.htm
tech.root: direct3d11
ms.assetid: 7E97B8EB-E674-4B90-9B9B-202552DBD95C
ms.date: 12/05/2018
ms.keywords: ID3D10Blob, ID3D10Blob interface [Direct3D 11], ID3D10Blob interface [Direct3D 11],described, d3dcommon/ID3D10Blob, direct3d11.id3d10blob
req.header: d3dcommon.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Blob
 - d3dcommon/ID3D10Blob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcommon.h
api_name:
 - ID3D10Blob
---

# ID3D10Blob interface


## -description

This interface is used to return arbitrary-length data.

## -inheritance

The <b>ID3D10Blob</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Blob</b> also has these types of members:

## -remarks

The <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface is type-defined in the D3DCommon.h header file as a <b>ID3D10Blob</b> interface, which is fully defined in the D3DCommon.h header file.
          <b>ID3DBlob</b> is version-neutral and can be used in code for any Direct3D version.
        

Blobs can be used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.
          Also, these objects are used to return object code and error messages in APIs that compile vertex, geometry and pixel shaders.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-interfaces">Common Version Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
