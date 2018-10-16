---
UID: NF:mfidl.IMFSensorTransformFactory.GetTransformCount
title: IMFSensorTransformFactory::GetTransformCount
author: windows-sdk-content
description: Called by the media pipeline to get the number of transforms provided by the sensor transform.
old-location: mf\imfsensortransformfactory_gettransformcount.htm
tech.root: medfound
ms.assetid: D1B1DA8D-9A59-43A0-9A2F-8749B2C05D37
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetTransformCount, GetTransformCount method [Media Foundation], GetTransformCount method [Media Foundation],IMFSensorTransformFactory interface, IMFSensorTransformFactory interface [Media Foundation],GetTransformCount method, IMFSensorTransformFactory.GetTransformCount, IMFSensorTransformFactory::GetTransformCount, mf.imfsensortransformfactory_gettransformcount, mfidl/IMFSensorTransformFactory::GetTransformCount
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
 - IMFSensorTransformFactory.GetTransformCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorTransformFactory::GetTransformCount


## -description


Called by the media pipeline to get the number of transforms provided by the sensor transform.


## -parameters




### -param pdwCount [in]

The number of transforms provided by the sensor transform.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the current release, chaining of transforms is not supported, so this value should always be 1.




## -see-also




<a href="https://msdn.microsoft.com/291EA582-22E3-4646-8E89-74162E98203F">IMFSensorTransformFactory</a>
 

 

