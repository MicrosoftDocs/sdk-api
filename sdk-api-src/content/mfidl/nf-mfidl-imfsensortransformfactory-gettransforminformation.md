---
UID: NF:mfidl.IMFSensorTransformFactory.GetTransformInformation
title: IMFSensorTransformFactory::GetTransformInformation method
author: windows-driver-content
description: Called by the media pipeline to get information about a transform provided by the sensor transform.
old-location: mf\imfsensortransformfactory_gettransforminformation.htm
old-project: medfound
ms.assetid: A83B0A75-60CF-49AA-9386-70A30189C009
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetTransformInformation method [Media Foundation], GetTransformInformation method [Media Foundation], IMFSensorTransformFactory interface, GetTransformInformation,IMFSensorTransformFactory.GetTransformInformation, IMFSensorTransformFactory, IMFSensorTransformFactory interface [Media Foundation], GetTransformInformation method, IMFSensorTransformFactory::GetTransformInformation, mf.imfsensortransformfactory_gettransforminformation, mfidl/IMFSensorTransformFactory::GetTransformInformation
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
-	IMFSensorTransformFactory.GetTransformInformation
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorTransformFactory::GetTransformInformation method


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

A collection of <a href="https://msdn.microsoft.com/9A5F6E25-796A-4798-8E4A-ABB9EB6A3B84">IMFSensorStream</a> objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/291EA582-22E3-4646-8E89-74162E98203F">IMFSensorTransformFactory</a>
 

 

