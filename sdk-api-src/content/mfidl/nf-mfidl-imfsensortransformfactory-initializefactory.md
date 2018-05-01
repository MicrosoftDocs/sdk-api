---
UID: NF:mfidl.IMFSensorTransformFactory.InitializeFactory
title: IMFSensorTransformFactory::InitializeFactory method
author: windows-driver-content
description: Called by the media pipeline to initialize the sensor transform.
old-location: mf\imfsensortransformfactory_initializefactory.htm
old-project: medfound
ms.assetid: 395BC62A-5A20-4C9D-A097-2DBEF6CD93C2
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFSensorTransformFactory, IMFSensorTransformFactory interface [Media Foundation], InitializeFactory method, IMFSensorTransformFactory::InitializeFactory, InitializeFactory method [Media Foundation], InitializeFactory method [Media Foundation], IMFSensorTransformFactory interface, InitializeFactory,IMFSensorTransformFactory.InitializeFactory, mf.imfsensortransformfactory_initializefactory, mfidl/IMFSensorTransformFactory::InitializeFactory
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorTransformFactory.InitializeFactory
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorTransformFactory::InitializeFactory method


## -description


Called by the media pipeline to initialize the sensor transform.


## -parameters




### -param dwMaxTransformCount [in]

The maximum number of transforms allowed in a single transform. In the current release, this is always 1.


### -param pSensorDevices [in]

A collection of <a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a> objects representing the available sensors.


### -param pAttributes [in, optional]

The attribute store to be populated by the sensor transform. The only required attribute for sensor transforms is <a href="https://msdn.microsoft.com/C9128AA0-E86B-4E83-8173-2568377235FB">MF_STF_VERSION_INFO</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/291EA582-22E3-4646-8E89-74162E98203F">IMFSensorTransformFactory</a>
 

 

