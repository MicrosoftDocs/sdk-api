---
UID: NF:mfidl.IMFSensorTransformFactory.GetTransformInformation
title: IMFSensorTransformFactory::GetTransformInformation (mfidl.h)
description: Called by the media pipeline to get information about a transform provided by the sensor transform.
old-location: mf\imfsensortransformfactory_gettransforminformation.htm
tech.root: medfound
ms.assetid: A83B0A75-60CF-49AA-9386-70A30189C009
ms.date: 12/05/2018
ms.keywords: GetTransformInformation, GetTransformInformation method [Media Foundation], GetTransformInformation method [Media Foundation],IMFSensorTransformFactory interface, IMFSensorTransformFactory interface [Media Foundation],GetTransformInformation method, IMFSensorTransformFactory.GetTransformInformation, IMFSensorTransformFactory::GetTransformInformation, mf.imfsensortransformfactory_gettransforminformation, mfidl/IMFSensorTransformFactory::GetTransformInformation
f1_keywords:
- mfidl/IMFSensorTransformFactory.GetTransformInformation
dev_langs:
- c++
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
- IMFSensorTransformFactory.GetTransformInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorTransformFactory::GetTransformInformation


## -description


Called by the media pipeline to get information about a transform provided by the  sensor transform.


## -parameters




### -param TransformIndex [in]

The index of the transform for which information is being requested. In the current release, this value will always be 0.


### -param pguidTransformId [out]

Gets the identifier for the transform.


### -param ppAttributes [out]

The attribute store to be populated.


### -param ppStreamInformation [out]

A collection of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a> objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory">IMFSensorTransformFactory</a>
 

 

