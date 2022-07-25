---
UID: NF:mfidl.IMFSensorTransformFactory.CreateTransform
title: IMFSensorTransformFactory::CreateTransform (mfidl.h)
description: Called by the media pipeline to create the transform.
helpviewer_keywords: ["CreateTransform","CreateTransform method [Media Foundation]","CreateTransform method [Media Foundation]","IMFSensorTransformFactory interface","IMFSensorTransformFactory interface [Media Foundation]","CreateTransform method","IMFSensorTransformFactory.CreateTransform","IMFSensorTransformFactory::CreateTransform","mf.imfsensortransformfactory_createtransform","mfidl/IMFSensorTransformFactory::CreateTransform"]
old-location: mf\imfsensortransformfactory_createtransform.htm
tech.root: mf
ms.assetid: 90F986B1-7E1A-43AC-A633-34DD9D53D634
ms.date: 12/05/2018
ms.keywords: CreateTransform, CreateTransform method [Media Foundation], CreateTransform method [Media Foundation],IMFSensorTransformFactory interface, IMFSensorTransformFactory interface [Media Foundation],CreateTransform method, IMFSensorTransformFactory.CreateTransform, IMFSensorTransformFactory::CreateTransform, mf.imfsensortransformfactory_createtransform, mfidl/IMFSensorTransformFactory::CreateTransform
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorTransformFactory::CreateTransform
 - mfidl/IMFSensorTransformFactory::CreateTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorTransformFactory.CreateTransform
---

# IMFSensorTransformFactory::CreateTransform


## -description

Called by the media pipeline to create the transform.

## -parameters

### -param guidSensorTransformID [in]

The identifier of the transform to be created.

### -param pAttributes [in, optional]

The identifier of the transform to be created.

### -param ppDeviceMFT [in, optional]

The identifier of the transform to be created.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory">IMFSensorTransformFactory</a>