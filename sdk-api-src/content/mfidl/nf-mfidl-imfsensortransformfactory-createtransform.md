---
UID: NF:mfidl.IMFSensorTransformFactory.CreateTransform
title: IMFSensorTransformFactory::CreateTransform
author: windows-sdk-content
description: Called by the media pipeline to create the transform.
old-location: mf\imfsensortransformfactory_createtransform.htm
tech.root: medfound
ms.assetid: 90F986B1-7E1A-43AC-A633-34DD9D53D634
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CreateTransform, CreateTransform method [Media Foundation], CreateTransform method [Media Foundation],IMFSensorTransformFactory interface, IMFSensorTransformFactory interface [Media Foundation],CreateTransform method, IMFSensorTransformFactory.CreateTransform, IMFSensorTransformFactory::CreateTransform, mf.imfsensortransformfactory_createtransform, mfidl/IMFSensorTransformFactory::CreateTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFSensorTransformFactory.CreateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorTransformFactory::CreateTransform


## -description


Called by the media pipeline to create the transform.


## -parameters




### -param guidSensorTransformID [in]

The identifier of the transform to be created.


### -param pAttributes [in, optional]

The identifier of the transform to be created.

The identifier of the transform to be created.


### -param ppDeviceMFT

TBD




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/291EA582-22E3-4646-8E89-74162E98203F">IMFSensorTransformFactory</a>
 

 

