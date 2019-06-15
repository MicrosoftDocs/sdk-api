---
UID: NF:mfidl.IMFSensorTransformFactory.InitializeFactory
title: IMFSensorTransformFactory::InitializeFactory (mfidl.h)
author: windows-sdk-content
description: Called by the media pipeline to initialize the sensor transform.
old-location: mf\imfsensortransformfactory_initializefactory.htm
tech.root: medfound
ms.assetid: 395BC62A-5A20-4C9D-A097-2DBEF6CD93C2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSensorTransformFactory interface [Media Foundation],InitializeFactory method, IMFSensorTransformFactory.InitializeFactory, IMFSensorTransformFactory::InitializeFactory, InitializeFactory, InitializeFactory method [Media Foundation], InitializeFactory method [Media Foundation],IMFSensorTransformFactory interface, mf.imfsensortransformfactory_initializefactory, mfidl/IMFSensorTransformFactory::InitializeFactory
ms.topic: method
f1_keywords: ["mfidl/IMFSensorTransformFactory.InitializeFactory"]
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
 - IMFSensorTransformFactory.InitializeFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorTransformFactory::InitializeFactory


## -description


Called by the media pipeline to initialize the sensor transform.


## -parameters




### -param dwMaxTransformCount [in]

The maximum number of transforms allowed in a single transform. In the current release, this is always 1.


### -param pSensorDevices [in]

A collection of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a> objects representing the available sensors.


### -param pAttributes [in, optional]

The attribute store to be populated by the sensor transform. The only required attribute for sensor transforms is <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-stf-version-info">MF_STF_VERSION_INFO</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory">IMFSensorTransformFactory</a>
 

 

