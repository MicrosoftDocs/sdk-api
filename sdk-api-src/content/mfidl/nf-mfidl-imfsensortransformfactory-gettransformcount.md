---
UID: NF:mfidl.IMFSensorTransformFactory.GetTransformCount
title: IMFSensorTransformFactory::GetTransformCount (mfidl.h)
description: Called by the media pipeline to get the number of transforms provided by the sensor transform.
helpviewer_keywords: ["GetTransformCount","GetTransformCount method [Media Foundation]","GetTransformCount method [Media Foundation]","IMFSensorTransformFactory interface","IMFSensorTransformFactory interface [Media Foundation]","GetTransformCount method","IMFSensorTransformFactory.GetTransformCount","IMFSensorTransformFactory::GetTransformCount","mf.imfsensortransformfactory_gettransformcount","mfidl/IMFSensorTransformFactory::GetTransformCount"]
old-location: mf\imfsensortransformfactory_gettransformcount.htm
tech.root: mf
ms.assetid: D1B1DA8D-9A59-43A0-9A2F-8749B2C05D37
ms.date: 12/05/2018
ms.keywords: GetTransformCount, GetTransformCount method [Media Foundation], GetTransformCount method [Media Foundation],IMFSensorTransformFactory interface, IMFSensorTransformFactory interface [Media Foundation],GetTransformCount method, IMFSensorTransformFactory.GetTransformCount, IMFSensorTransformFactory::GetTransformCount, mf.imfsensortransformfactory_gettransformcount, mfidl/IMFSensorTransformFactory::GetTransformCount
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
 - IMFSensorTransformFactory::GetTransformCount
 - mfidl/IMFSensorTransformFactory::GetTransformCount
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
 - IMFSensorTransformFactory.GetTransformCount
---

# IMFSensorTransformFactory::GetTransformCount


## -description

Called by the media pipeline to get the number of transforms provided by the sensor transform.

## -parameters

### -param pdwCount [in]

The number of transforms provided by the sensor transform.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the current release, chaining of transforms is not supported, so this value should always be 1.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory">IMFSensorTransformFactory</a>