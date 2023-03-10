---
UID: NF:xpsobjectmodel_2.IXpsOMPackageWriter3D.AddModelTexture
title: IXpsOMPackageWriter3D::AddModelTexture (xpsobjectmodel_2.h)
description: Creates a new 3D model texture from the specified texture part and stream.
helpviewer_keywords: ["AddModelTexture","AddModelTexture method [XPS Documents and Packaging]","AddModelTexture method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","AddModelTexture method","IXpsOMPackageWriter3D.AddModelTexture","IXpsOMPackageWriter3D::AddModelTexture","xps.ixpsompackagewriter3d_addmodeltexture","xpsobjectmodel_2/IXpsOMPackageWriter3D::AddModelTexture"]
old-location: xps\ixpsompackagewriter3d_addmodeltexture.htm
tech.root: xps
ms.assetid: 76FC9938-914C-4328-BE71-DC898241D9EA
ms.date: 12/05/2018
ms.keywords: AddModelTexture, AddModelTexture method [XPS Documents and Packaging], AddModelTexture method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],AddModelTexture method, IXpsOMPackageWriter3D.AddModelTexture, IXpsOMPackageWriter3D::AddModelTexture, xps.ixpsompackagewriter3d_addmodeltexture, xpsobjectmodel_2/IXpsOMPackageWriter3D::AddModelTexture
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_2.idl
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
 - IXpsOMPackageWriter3D::AddModelTexture
 - xpsobjectmodel_2/IXpsOMPackageWriter3D::AddModelTexture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsObjectModel_2.h
api_name:
 - IXpsOMPackageWriter3D.AddModelTexture
---

# IXpsOMPackageWriter3D::AddModelTexture


## -description

Creates a new 3D model texture from the specified texture part and stream.

## -parameters

### -param texturePartName [in]

The Open Package Convention (OPC)  name of the texture part. This part is added to the package and becomes a relationship target of the model part.

### -param textureData [in]

A readable stream which holds 3D model texture. When calling this method, you must provide PNG or JPEG data.

## -returns

Returns the appropriate HRESULT error code.

## -remarks

Each time this method is called, it creates a new part with a specified name, content and hardcoded content type “application/vnd.ms-package.3dmanufacturing-3dmodeltexture”. That part is linked from the model part with relationship type “http://schemas.microsoft.com/3dmanufacturing/2013/01/3dmodeltexture”.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>