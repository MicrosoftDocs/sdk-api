---
UID: NF:d2d1.ID2D1Mesh.Open
title: ID2D1Mesh::Open (d2d1.h)
description: Opens the mesh for population.
helpviewer_keywords: ["ID2D1Mesh interface [Direct2D]","Open method","ID2D1Mesh.Open","ID2D1Mesh::Open","Open","Open method [Direct2D]","Open method [Direct2D]","ID2D1Mesh interface","d2d1/ID2D1Mesh::Open","direct2d.ID2D1Mesh_Open"]
old-location: direct2d\ID2D1Mesh_Open.htm
tech.root: Direct2D
ms.assetid: 7cd0d637-7fcd-45a5-932f-5aa8fb476f68
ms.date: 12/05/2018
ms.keywords: ID2D1Mesh interface [Direct2D],Open method, ID2D1Mesh.Open, ID2D1Mesh::Open, Open, Open method [Direct2D], Open method [Direct2D],ID2D1Mesh interface, d2d1/ID2D1Mesh::Open, direct2d.ID2D1Mesh_Open
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Mesh::Open
 - d2d1/ID2D1Mesh::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Mesh.Open
---

# ID2D1Mesh::Open


## -description

Opens the mesh for population.

## -parameters

### -param tessellationSink [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a>**</b>

When this method returns, contains a pointer to a pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a> that is used to populate the mesh. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1mesh">ID2D1Mesh</a>

